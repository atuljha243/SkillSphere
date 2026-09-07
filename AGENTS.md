# AGENTS.md — SMART CAMPUS AI AGENT GUIDELINES

**Version:** 1.0  
**Purpose:** Guide AI agents (Antigravity, Claude, etc.) on how to work on Smart Campus  
**Authority:** This is the law for all agent implementation

---

## 🤖 UNIVERSAL AGENT RULES

### Rule 1: READ BEFORE YOU CODE
Before implementing ANY chunk:
1. Read EXECUTION_LOG.md (what's been done)
2. Read PROJECT_PLAN.md (the vision)
3. Read MVP_SCOPE.md (what we're building)
4. Read API.md (the contract)
5. Read ARCHITECTURE.md (how it works)
6. Read DATABASE.md (the schema)
7. Read this file (AI_RULES.md)
8. Read PROJECT_PROGRESS.md (current state)
9. Read TESTING.md (what tests are needed)

**DO NOT START UNTIL YOU'VE READ ALL 9 FILES.**

### Rule 2: ONE CHUNK AT A TIME
- ✅ DO: Implement exactly what the chunk asks for
- ❌ DON'T: Look ahead to future chunks
- ❌ DON'T: Implement "while we're at it" features
- ❌ DON'T: Refactor previous work unless specifically requested

### Rule 3: THE API IS SACRED
- ✅ DO: Follow API.md exactly
- ❌ DON'T: Invent new endpoints
- ❌ DON'T: Change request/response schemas
- ❌ DON'T: Add undocumented parameters

If the chunk requires a new API:
1. Update API.md first
2. Document the new endpoint
3. THEN implement it
4. Update PROJECT_PROGRESS.md
5. Commit the change

### Rule 4: TESTS BEFORE COMPLETION
- ✅ Every chunk must have tests
- ✅ Tests must PASS before claiming done
- ✅ Report exact pass/fail numbers
- ❌ DON'T claim "done" with failing tests

### Rule 5: NO BREAKING CHANGES
- ✅ DO: Preserve existing functionality
- ✅ DO: Keep backward compatibility
- ❌ DON'T: Modify existing database tables without migration
- ❌ DON'T: Change existing API responses
- ❌ DON'T: Delete working code

### Rule 6: DOCUMENTATION IS NOT OPTIONAL
After EVERY chunk update:
- [ ] PROJECT_PROGRESS.md
- [ ] CHANGELOG.md
- [ ] Relevant .md files if APIs changed
- [ ] Code comments for complex logic
- [ ] Commit message is descriptive

### Rule 7: GIT DISCIPLINE
After every chunk:
```bash
git add .
git commit -m "chunk-X: module-name with brief description"
git push
```

Never commit without a clear message.

### Rule 8: REPORT FORMAT
At the end of every chunk, provide:

```
CHUNK: X
STATUS: COMPLETE ✅ / IN PROGRESS ⏳ / BLOCKED 🚫

IMPLEMENTED:
✅ Feature 1
✅ Feature 2
✅ Feature 3

FILES CREATED:
• path/to/file1.py
• path/to/file2.js
• path/to/file3.sql

FILES MODIFIED:
• path/to/modified.py

DATABASE CHANGES:
- Created: users table
- Modified: None
- Deleted: None

APIs CREATED/MODIFIED:
- POST /api/v1/auth/login (NEW)
- GET /api/v1/health (NEW)

TESTS:
✅ Passed: 12
❌ Failed: 0
⏭️ Skipped: 0

KNOWN ISSUES:
- Issue description (workaround: ...)

DOCUMENTATION UPDATED:
✅ PROJECT_PROGRESS.md
✅ CHANGELOG.md
✅ API.md (if APIs added)

NEXT CHUNK:
Chunk X+1: Module Name - Brief description

GIT COMMIT:
chunk-X: module-name completed with X tests passing
```

---

## 🔍 AGENT DECISION TREE

### When starting a chunk:

```
1. Read all 9 foundational files?
   ├─ NO → Stop, read them first
   └─ YES → Continue

2. Do you understand the chunk requirement?
   ├─ NO → Document ambiguity, stop
   └─ YES → Continue

3. Is this chunk dependent on previous chunks?
   ├─ YES, previous not done → Stop, wait for prerequisites
   └─ NO or prerequisites done → Continue

4. Do you need API keys?
   ├─ YES → Check .env.example
   ├─ Keys missing? → Stop, ask for them
   └─ Keys available → Continue

5. Can you implement without breaking existing code?
   ├─ NO → Stop, redesign approach
   └─ YES → Implement

6. Did you write tests?
   ├─ NO → Write tests
   └─ YES → Run tests

7. Do all tests pass?
   ├─ NO → Fix code, retest
   └─ YES → Continue

8. Did you update documentation?
   ├─ NO → Update PROJECT_PROGRESS.md, CHANGELOG.md
   └─ YES → Continue

9. Ready to commit?
   ├─ All above done → Commit
   └─ Something missing → Go back to step that failed
```

---

## 🚫 AGENT ANTI-PATTERNS

### ❌ DON'T DO THIS

```
❌ Jump to CHUNK 50 because it sounds cool
❌ Implement microservices when monolith specified
❌ Add dependencies not in the tech stack
❌ Call AI endpoints 100 times when caching could help
❌ Hardcode secrets in code
❌ Skip tests to move faster
❌ Modify database schema without migration
❌ Change API contracts without updating API.md
❌ Refactor other chunks' code
❌ Leave debugging statements in production code
❌ Claim completion with failing tests
❌ Commit without clear messages
❌ Create "helper" files not requested
❌ Add "nice to have" features
```

---

## ✅ AGENT BEST PRACTICES

### ✅ DO THIS

```
✅ Read all documentation before coding
✅ Implement exactly what's requested
✅ Write tests alongside code
✅ Make tests pass before claiming done
✅ Update PROJECT_PROGRESS.md immediately
✅ Use meaningful commit messages
✅ Cache AI results in database
✅ Follow API.md exactly
✅ Keep functions small and testable
✅ Add clear error messages
✅ Use environment variables for config
✅ Document why, not just what
✅ Test edge cases
✅ Respect RBAC in all APIs
✅ Use transactions for multi-step operations
```

---

## 🎯 AI SERVICE USAGE RULES

### When AI is ALLOWED:

| Feature | Provider | When | Cache |
|---------|----------|------|-------|
| Resume Generation | Gemini | On demand | ✅ Yes, in DB |
| Skill Extraction | Groq/Gemini | On project submit | ✅ Yes, in DB |
| Certificate OCR | Gemini | On upload | ✅ Yes, store result |
| Resume Gap Analysis | Gemini | On request | ✅ Yes, cache |
| RAG Query | Gemini | On search | ✅ Yes, store chunks |
| Decision Copilot | Gemini | On query | ✅ Yes, cache answers |
| Expertise Matching | Embeddings | Search only | ✅ Yes, precompute |

### When AI is FORBIDDEN:

```
❌ Authentication decision
❌ Timetable conflict detection
❌ Room availability check
❌ Attendance calculation
❌ Placement eligibility
❌ Official state changes
❌ Admin approval workflows
❌ Data validation
❌ Impact analysis
❌ Incident categorization (deterministic only)
```

### AI Call Caching Strategy:

```
INPUT
  ↓
Check database for cached result
  ├─ FOUND → Return cached result
  └─ NOT FOUND → Continue
  ↓
Call AI service
  ↓
Store result in database with TTL
  ↓
Return result
```

**Never call AI twice for the same input.**

---

## 🔐 SECURITY RULES FOR AGENTS

### Secrets Management
- ✅ Store secrets in .env
- ✅ Load from environment at runtime
- ✅ Use environment variables in code
- ❌ Never hardcode secrets
- ❌ Never log secrets
- ❌ Never send secrets to frontend

### API Key Rules
- ✅ GEMINI_API_KEY in backend only
- ✅ GROQ_API_KEY in backend only
- ✅ JWT_SECRET in backend only
- ✅ DATABASE passwords in .env
- ❌ NO API keys in React code
- ❌ NO secrets in Git commits
- ❌ NO secrets in error messages

### Authorization Rules
- ✅ Check role on server side
- ✅ Enforce RBAC on every endpoint
- ✅ Student can only read own data
- ✅ Faculty can only read assigned classes
- ✅ Admin has full access
- ❌ Never trust frontend role claims
- ❌ Never skip authorization checks

### Data Validation
- ✅ Validate all input
- ✅ Sanitize file uploads
- ✅ Use parameterized queries
- ✅ Escape special characters
- ✅ Validate email format
- ✅ Validate UUID format
- ✅ Check date ranges
- ❌ Never trust frontend validation

---

## 📊 METRICS & EXPECTATIONS

### Per Chunk Expectations:
- Time to implement: 2-4 hours
- Lines of code: 200-500
- Test coverage: >80% of logic
- Tests passing: 100%
- Documentation: 100% of APIs
- Git commits: 1 clean commit per chunk

### Code Quality Standards:
- No console.log/print debugging
- No commented-out code
- Clear variable names
- Functions <50 lines
- Maximum nesting: 3 levels
- Error handling for all operations
- Input validation on all APIs

### Test Requirements:
- Unit tests for business logic
- Integration tests for APIs
- Happy path test
- Error path test
- Edge case test
- RBAC test (if applicable)

---

## 🚨 WHEN TO STOP & ASK

**Stop immediately and ask if:**

1. **Ambiguous requirement** - Chunk description unclear
2. **Missing dependency** - Previous chunk not done
3. **API key needed** - GEMINI_API_KEY or GROQ_API_KEY required
4. **Breaking change needed** - Would break existing APIs
5. **Schema migration needed** - Database structure change required
6. **External service needed** - Third party service not yet integrated
7. **Conflicting requirements** - Two rules contradict each other
8. **Resource limit reached** - Can't complete in reasonable time

**Example stop message:**
```
STOPPED: Cannot implement CHUNK 21 without GEMINI_API_KEY.
Please provide GEMINI_API_KEY in .env to proceed.
```

---

## 📋 FINAL AGENT CHECKLIST

Before claiming CHUNK COMPLETE:

- [ ] Read all 9 documentation files
- [ ] Understood the chunk requirement
- [ ] All dependencies completed
- [ ] All API keys available
- [ ] Code written following standards
- [ ] Tests written (>80% logic)
- [ ] All tests passing (100%)
- [ ] No secrets in code
- [ ] RBAC enforced where needed
- [ ] PROJECT_PROGRESS.md updated
- [ ] CHANGELOG.md updated
- [ ] Relevant API.md updated (if new endpoints)
- [ ] Code comments added
- [ ] Git commit made
- [ ] Report format provided

**If ANY checkbox unchecked: DO NOT CLAIM COMPLETE**

---

## 🎯 SUMMARY FOR AGENTS

**You are implementing Smart Campus incrementally.**

Each chunk is:
- ✅ Self-contained
- ✅ Tested
- ✅ Documented
- ✅ Committed
- ✅ Then: NEXT CHUNK

**Never:**
- Skip tests
- Break existing code
- Invent features
- Jump ahead
- Ignore documentation
- Hardcode secrets
- Change API contracts

**Always:**
- Read docs first
- Follow the chunk request exactly
- Write tests that pass
- Update PROJECT_PROGRESS.md
- Make clean commits
- Report in the standard format
- Ask before implementing breaking changes

---

**This file is LAW for all agents working on Smart Campus.**

No agent may proceed without acknowledging these rules.

