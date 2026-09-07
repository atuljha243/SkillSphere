# SMART CAMPUS — ANTIGRAVITY MODULE PROMPT PACK

## UNIVERSAL HEADER — USE WITH EVERY CHUNK

You are working on the Smart Campus project.

Before doing anything:

1. Read AGENTS.md
2. Read PROJECT_SPEC.md
3. Read ARCHITECTURE.md
4. Read API.md
5. Read DATABASE.md
6. Read PROJECT_PROGRESS.md
7. Read AI_RULES.md

You are implementing ONLY the requested chunk.

**STRICT RULES:**

- ✅ Do ONLY the requested chunk
- ❌ Do NOT implement future chunks
- ❌ Do NOT rewrite working modules unnecessarily
- ❌ Do NOT invent requirements
- ❌ Do NOT invent API contracts
- ❌ Do NOT silently change database schema
- ❌ Do NOT silently change architecture
- ❌ Do NOT add unnecessary dependencies
- ✅ Reuse existing abstractions
- ✅ Preserve existing functionality
- ✅ Keep implementation production-quality but hackathon-scoped
- ❌ Never put secrets in source code
- ❌ Never expose API keys in frontend code
- ✅ Add tests for new business logic
- ✅ Run tests before completion
- ✅ Fix blocking failures before stopping
- ✅ Update PROJECT_PROGRESS.md
- ✅ Update CHANGELOG.md
- ✅ Update relevant documentation
- ✅ Report changed files, APIs, DB changes and test results
- ✅ STOP after the requested chunk

**If requirements are unclear:** Check project documents first. If still ambiguous, document the ambiguity and stop.

---

## 70 CHUNK ROADMAP

| Phase | Module | Focus | Status |
|-------|--------|-------|--------|
| 1 | Repository Bootstrap | Docs & structure | ⏳ Ready |
| 2 | Frontend Foundation | React + Vite shell | ⏳ Ready |
| 3 | Backend Foundation | Spring Boot REST | ⏳ Ready |
| 4 | SQLite Setup | Database config | ⏳ Ready |
| 5 | Docker Foundation | Containerization | ⏳ Ready |
| 6 | Authentication + RBAC | Login & roles | ⏳ Ready |
| 7 | College/Dept Model | Basic entities | ⏳ Ready |
| 8 | Campus Structure | Buildings/Rooms | ⏳ Ready |
| 9 | Subjects + Classes | Academic setup | ⏳ Ready |
| 10 | Timetable Foundation | CRUD only | ⏳ Ready |
| 11 | Timetable Conflicts | Deterministic checks | ⏳ Ready |
| 12 | Timetable Generator | Basic scheduling | ⏳ Ready |
| 13 | Student Academics | Attendance/Exams | ⏳ Ready |
| 14 | Attendance Engine | Calculations | ⏳ Ready |
| 15 | PYQ Search | Metadata & filtering | ⏳ Ready |
| 16 | Assignments | CRUD & status | ⏳ Ready |
| 17 | Events | Registration & tracking | ⏳ Ready |
| 18 | Event Intelligence | Prediction engine | ⏳ Ready |
| 19 | Communication Engine | Announcements & targeting | ⏳ Ready |
| 20 | Student Profile | Skills/Projects/Achievements | ⏳ Ready |
| 21 | Project→Skill Extraction | AI-assisted (Groq/Gemini) | ⏳ Ready |
| 22 | Achievement+Certificate | Upload & verification | ⏳ Ready |
| 23 | Placements | Opportunity CRUD | ⏳ Ready |
| 24 | Placement Eligibility | Deterministic matching | ⏳ Ready |
| 25 | Opportunity Matching | Skill-based scoring | ⏳ Ready |
| 26 | Resume Generator | AI synthesis (Gemini) | ⏳ Ready |
| 27 | Resume Gap Analyzer | AI interpretation | ⏳ Ready |
| 28 | Career Twin | Profile + what-if | ⏳ Ready |
| 29 | Expertise Search | Structured query | ⏳ Ready |
| 30 | Expertise Matching | Semantic + structured | ⏳ Ready |
| 31 | Support Requests | CRUD + routing | ⏳ Ready |
| 32 | Infrastructure Incidents | Issue reporting | ⏳ Ready |
| 33 | Duplicate Detection | Similar issue finding | ⏳ Ready |
| 34 | Recurring Issues | Historical analysis | ⏳ Ready |
| 35 | Live Room Availability | Real-time status | ⏳ Ready |
| 36 | Emergency Room Rescue | Alternative finding | ⏳ Ready |
| 37 | Room Rescue Approval | Transactional update | ⏳ Ready |
| 38 | Campus Impact Engine | Room unavailability | ⏳ Ready |
| 39 | Block Impact | Building unavailability | ⏳ Ready |
| 40 | What-If Simulation | Read-only scenarios | ⏳ Ready |
| 41 | Campus Data Health | Anomaly detection | ⏳ Ready |
| 42 | Silent Problem Detector | Hidden issue signals | ⏳ Ready |
| 43 | Bottleneck Detector | Resource pressure | ⏳ Ready |
| 44 | Campus Live State | Dashboard state | ⏳ Ready |
| 45 | Campus Digital Twin UI | Visual representation | ⏳ Ready |
| 46 | Campus State Animation | Meaningful visuals | ⏳ Ready |
| 47 | Campus Memory | Historical persistence | ⏳ Ready |
| 48 | College Knowledge Base | Document management | ⏳ Ready |
| 49 | RAG Ingestion | Document processing | ⏳ Ready |
| 50 | RAG Embeddings | Embedding generation | ⏳ Ready |
| 51 | ChromaDB Setup | Vector store config | ⏳ Ready |
| 52 | RAG Retrieval | Vector search | ⏳ Ready |
| 53 | RAG Generation | Grounded answers | ⏳ Ready |
| 54 | PYQ Semantic Search | Question retrieval | ⏳ Ready |
| 55 | Digital Library Config | Admin settings | ⏳ Ready |
| 56 | Library Reservation | Seat booking | ⏳ Ready |
| 57 | Smart Action Engine | Prioritized actions | ⏳ Ready |
| 58 | Decision Copilot | Natural language queries | ⏳ Ready |
| 59 | Global Search | Unified search | ⏳ Ready |
| 60 | Admin Dashboard | Operational view | ⏳ Ready |
| 61 | Faculty Dashboard | Schedule + class view | ⏳ Ready |
| 62 | Student Dashboard Integration | Personalized home | ⏳ Ready |
| 63 | Complete Room Emergency Demo | Full workflow test | ⏳ Ready |
| 64 | Complete Event Demo | Full event flow | ⏳ Ready |
| 65 | End-to-End Testing | Integration tests | ⏳ Ready |
| 66 | Security Review | Auth & validation | ⏳ Ready |
| 67 | Docker Hardening | Production readiness | ⏳ Ready |
| 68 | Deployment Preparation | AWS readiness | ⏳ Ready |
| 69 | Demo Polish | UI/UX refinement | ⏳ Ready |
| 70 | Final Integration | Complete system test | ✅ Ready |

---

## CHUNK DETAILS

### CHUNK 1 — REPOSITORY BOOTSTRAP ✅

**What to do:**
- Create documentation files
- Initialize Git repository
- Setup basic project structure
- Create .env.example
- Update PROJECT_PROGRESS.md

**No business logic**

**STOP after this chunk**

---

### CHUNK 2 — FRONTEND FOUNDATION ✅

**What to do:**
```
React + Vite setup
├── Router configuration
├── Base layout shell
├── Navigation (Student/Faculty/Admin)
├── API client abstraction
├── Global loading state
├── Global error state
└── Error boundary
```

**No business features**

**Run:** `npm install && npm run build`

---

### CHUNK 3 — BACKEND FOUNDATION ✅

**What to do:**
```
Spring Boot REST API
├── Configuration
├── Validation framework
├── Global exception handler
├── Standard response format
├── GET /api/v1/health
├── Logging setup
└── Test foundation
```

**Run all tests**

---

### CHUNK 4 — SQLITE SETUP ✅

**What to do:**
```
SQLite configuration
├── File-based persistence
├── Environment-based paths
├── JPA setup
├── Connection pool
├── Health check
└── Basic repository test
```

**No business entities yet**

---

### CHUNK 5 — DOCKER FOUNDATION ✅

**What to do:**
```
Containerization
├── Dockerfile (frontend)
├── Dockerfile (backend)
├── docker-compose.yml
├── Environment variables
├── Health checks
├── Persistent volumes
└── Service networking
```

**Verify:**
```bash
docker compose build
docker compose up -d
docker compose ps
```

---

### CHUNK 6 — AUTHENTICATION + RBAC ✅

**Roles:**
```
STUDENT
FACULTY
EVENT_COORDINATOR
DEPARTMENT_ADMIN
PLACEMENT_ADMIN
LIBRARIAN
COLLEGE_ADMIN
```

**What to do:**
```
├── User entity
├── Role entity
├── Login endpoint
├── JWT tokens
├── Authorization middleware
├── Current user endpoint
└── Role-based access control
```

**Tests:**
- Valid login ✓
- Invalid login ✓
- Student access ✓
- Forbidden access ✓
- Admin access ✓

---

### CHUNK 7 — COLLEGE / DEPARTMENT MODEL ✅

**What to do:**
```
├── College entity
├── Department entity
├── Student entity
├── Faculty entity
├── Relationships
├── Seed demo data
└── Basic CRUD tests
```

---

### CHUNK 8 — CAMPUS STRUCTURE ✅

**What to do:**
```
├── Building
├── Floor
├── Room (Classroom/Lab/Auditorium)
├── Equipment
├── Status tracking
├── Seed data:
│   ├── 3 buildings
│   ├── 6 floors
│   ├── 25 rooms
│   ├── 5 labs
│   ├── 1 auditorium
│   └── 1 library
└── Tests
```

---

## API KEY & CONFIGURATION REQUIREMENTS

You will need to provide when requested:

### Before CHUNK 21 (Project Skill Extraction):
- [ ] GEMINI_API_KEY (Google Gemini)
- [ ] GROQ_API_KEY (Groq)

### Before CHUNK 26 (Resume Generation):
- [ ] GEMINI_API_KEY (confirmed working)

### Before CHUNK 48+ (RAG):
- [ ] ChromaDB running (Docker)
- [ ] GEMINI_API_KEY or alternative embedding model

---

## AI SERVICE PROVIDER STRATEGY

| Feature | Provider | Why |
|---------|----------|-----|
| Project skill extraction | Groq/Gemini | Fast, low-cost |
| Certificate extraction | Gemini | OCR quality |
| Resume generation | Gemini | Semantic generation |
| Resume analysis | Gemini/Groq | Interpretation |
| RAG (College KB) | Gemini | Long context, quality |
| PYQ generation | Gemini | Academic context |
| Decision Copilot | Gemini | Complex reasoning |
| Expertise matching | Embeddings | Vector similarity |

---

## EXECUTION FLOW FOR YOU

### Phase 1: Setup & Configuration
**Your actions:**
1. ✅ Approve CHUNK 1-5 execution
2. Provide GEMINI_API_KEY when asked (before CHUNK 21)
3. Provide GROQ_API_KEY when asked (before CHUNK 21)
4. Verify Docker setup works

### Phase 2: Core Business Logic
**Chunks 6-62:**
- No additional API keys needed
- Pure business logic
- Deterministic algorithms
- Database operations

### Phase 3: Intelligence Features
**Chunks 21-62:**
- AI calls cached in database
- Reuse results where possible
- Batch operations where feasible

### Phase 4: RAG & Advanced Features
**Chunks 48-59:**
- ChromaDB configuration
- Embedding generation
- Semantic search

---

## .ENV TEMPLATE

You will need to set these:

```env
# Backend Configuration
SERVER_PORT=8080
DATABASE_PATH=/app/data/smart-campus.db
JWT_SECRET=your-jwt-secret-here
JWT_EXPIRATION=3600

# API Keys (provide when requested)
GEMINI_API_KEY=
GROQ_API_KEY=

# ChromaDB Configuration
CHROMA_HOST=chromadb
CHROMA_PORT=8000
CHROMA_API_KEY=

# Frontend Configuration
FRONTEND_URL=http://localhost:5173
API_BASE_URL=http://localhost:8080/api/v1
```

---

## TESTING REQUIREMENTS

Each chunk must have:
- ✅ Unit tests for business logic
- ✅ Integration tests for APIs
- ✅ All tests passing before completion
- ✅ Coverage for critical paths

---

## GIT WORKFLOW

After each chunk:

```bash
git add .
git commit -m "chunk-X: module-name completed"
git push
```

---

## DOCUMENTATION TO MAINTAIN

- ✅ AGENTS.md
- ✅ PROJECT_SPEC.md
- ✅ ARCHITECTURE.md
- ✅ API.md
- ✅ DATABASE.md
- ✅ PROJECT_PROGRESS.md
- ✅ CHANGELOG.md
- ✅ README.md
- ✅ AI_RULES.md
- ✅ TESTING.md

**All updated after each chunk.**

---

## CHECKPOINT: READY TO START?

**Before we begin CHUNK 1, confirm:**

1. ✅ You understand the 70-chunk roadmap
2. ✅ You will provide API keys when requested
3. ✅ You understand each chunk completes before next chunk starts
4. ✅ You will verify tests pass before marking complete
5. ✅ You will review module output before proceeding

**When ready, respond:**

```
APPROVED: Start CHUNK 1 - Repository Bootstrap
```

Then I will:
1. Create all documentation files
2. Initialize Git
3. Setup project structure
4. Create .env.example
5. Update PROJECT_PROGRESS.md
6. Commit everything

**Ready?**

