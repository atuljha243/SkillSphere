# SMART CAMPUS — PROJECT PLAN

**Repository:** atuljha243/SkillSphere  
**Tech Stack:** Python Flask, React JS, Chroma DB (RAG), SQLite  
**Status:** Planning Phase  
**Date Created:** 2026-09-07

---

## 1. PROJECT VISION

Smart Campus is a **Personalized Digital Campus Operating Platform** that connects students, faculty, administrators, departments, buildings, rooms, labs, timetables, subjects, classes, attendance, exams, assignments, events, library, infrastructure, placements, projects, achievements, and alumni into one unified, intelligent system.

**Core Principle:** PLANNED ≠ ACTUAL

The platform should continuously identify gaps between what was planned and what actually happened, turning them into actionable insights.

---

## 2. TECH STACK

| Component | Technology |
|-----------|-----------|
| **Frontend** | React JS |
| **Backend** | Python Flask |
| **Database (Primary)** | SQLite (local development) |
| **Vector DB (RAG)** | Chroma DB |
| **Containerization** | Docker + Docker Compose |
| **AI/LLM Integration** | RAG Layer (Chroma + LLM) |

---

## 3. CORE INTELLIGENCE SYSTEMS

1. Campus Digital Twin
2. Campus Relationship / Knowledge Graph
3. Live Campus State
4. Emergency Room Rescue
5. Campus Impact Engine
6. What-If Simulator
7. Silent Problem Detector
8. Campus Data Health Engine
9. Campus Bottleneck Detection
10. Campus Memory
11. Campus Expertise Graph
12. Student Career Twin
13. Smart Action Engine
14. Decision Copilot
15. Opportunity Matching

---

## 4. KEY USERS / ROLES

- **Student** - Access academics, placements, campus info, events
- **Faculty** - Manage classes, timetable, students
- **Event Coordinator** - Plan and manage events, track attendance
- **HOD / Department Admin** - Manage department operations
- **Placement Cell** - Track placements and internships
- **Librarian** - Manage library operations
- **College Administrator** - System-wide oversight and configuration

---

## 5. HIGH-LEVEL ARCHITECTURE

```
                         USERS
                           │
       ┌───────────────────┼───────────────────┐
       ↓                   ↓                   ↓
    STUDENT             FACULTY              ADMIN
       │                   │                   │
       └───────────────────┼───────────────────┘
                           ↓
                    REACT FRONTEND
                           │
                    REST / WEBSOCKET
                           ↓
                   FLASK BACKEND
                           │
        ┌──────────────────┼──────────────────┐
        ↓                  ↓                  ↓
    SQLite            Chroma DB          Integrations
   DATABASE           RAG LAYER
        │                  │
        └───────────┬──────┘
                    ↓
             CAMPUS DATA LAYER
                    ↓
          CAMPUS INTELLIGENCE
                    │
      ┌─────────────┼─────────────┐
      ↓             ↓             ↓
  Prediction    Detection      Matching
      ↓             ↓             ↓
  Optimization    Impact      Recommendation
      └─────────────┼─────────────┘
                    ↓
              HUMAN APPROVAL
                    ↓
                  ACTION
                    ↓
              ACTUAL OUTCOME
                    ↓
              CAMPUS MEMORY
```

---

## 6. DEVELOPMENT CHUNKS (32 Phases)

### CRITICAL RULE
**DO NOT BUILD ENTIRE PROJECT AT ONCE**

Build incrementally in clearly defined modules/chunks. For every chunk:
1. Inspect current repository state
2. Implement ONLY the requested module
3. Do NOT rewrite working modules unnecessarily
4. Preserve backward compatibility
5. Run application after implementation
6. Run relevant tests
7. Fix all blocking errors
8. Update documentation
9. Commit stable chunk to Git

### CHUNK SEQUENCE

| Phase | Name | Priority | Status |
|-------|------|----------|--------|
| 1 | Foundation + Docker + SQLite + React/Flask Shell | P0 | ⏳ Pending |
| 2 | Authentication + RBAC | P0 | ⏳ Pending |
| 3 | College Structure / Digital Campus Model | P0 | ⏳ Pending |
| 4 | Timetable + Scheduling Foundation | P0 | ⏳ Pending |
| 5 | Live Room Availability | P0 | ⏳ Pending |
| 6 | Emergency Room Rescue | P1 | ⏳ Pending |
| 7 | Student Academics + Attendance + Exams + Assignments + PYQs | P0 | ⏳ Pending |
| 8 | Events + Registration + Volunteers | P0 | ⏳ Pending |
| 9 | Event Intelligence | P1 | ⏳ Pending |
| 10 | Communication + Notifications | P0 | ⏳ Pending |
| 11 | Student Profile + Projects + Achievements | P0 | ⏳ Pending |
| 12 | Placements + Eligibility + Opportunity Matching | P0 | ⏳ Pending |
| 13 | Resume + Career Twin | P1 | ⏳ Pending |
| 14 | Alumni + Faculty Mentorship + Expertise Graph | P1 | ⏳ Pending |
| 15 | Support + Requests + Issue Intelligence | P0 | ⏳ Pending |
| 16 | Infrastructure + Maintenance + Recurring Issues | P1 | ⏳ Pending |
| 17 | Campus Data Health | P1 | ⏳ Pending |
| 18 | Silent Problem Detector | P1 | ⏳ Pending |
| 19 | Campus Live State + Digital Twin | P1 | ⏳ Pending |
| 20 | Campus Impact Engine | P1 | ⏳ Pending |
| 21 | What-If Simulator | P1 | ⏳ Pending |
| 22 | Campus Memory | P1 | ⏳ Pending |
| 23 | Decision Copilot | P2 | ⏳ Pending |
| 24 | College Knowledge Base + RAG (Chroma DB) | P2 | ⏳ Pending |
| 25 | Global Search | P1 | ⏳ Pending |
| 26 | Digital Library Configuration | P0 | ⏳ Pending |
| 27 | Library Occupancy / Reservation | P0 | ⏳ Pending |
| 28 | Analytics Dashboard | P2 | ⏳ Pending |
| 29 | Integration Testing | P0 | ⏳ Pending |
| 30 | Docker Production Hardening | P0 | ⏳ Pending |
| 31 | Deployment Preparation | P3 | ⏳ Pending |
| 32 | Demo Polish + Final Optimization | P3 | ⏳ Pending |

---

## 7. HACKATHON PRIORITY

### P0 — MUST WORK
1. Authentication / RBAC
2. Student Home
3. Academics (Timetable, Attendance, Exams)
4. Events
5. Placements
6. Student Profile
7. Projects / Achievements
8. Basic Campus Structure
9. Room Availability
10. Digital Library Configuration
11. Docker Setup

### P1 — MAJOR DIFFERENTIATION
12. Timetable Optimization
13. Emergency Room Rescue
14. Event Prediction
15. Campus Impact Engine
16. Live Campus State
17. Data Health
18. Silent Problem Detector

### P2 — ADVANCED DIFFERENTIATION
19. What-If Simulator
20. Expertise Graph
21. Career Twin
22. Campus Memory
23. Decision Copilot
24. RAG Knowledge Base

### P3 — POLISH / FUTURE
25. Advanced 3D Campus
26. Computer Vision Occupancy
27. Advanced Transport Routing
28. Advanced Predictive Maintenance
29. Advanced External Integrations

---

## 8. STUDENT UI NAVIGATION

Primary navigation (6 sections):

1. **HOME** - Personalized action center
2. **ACADEMICS** - Schedule, attendance, exams, assignments
3. **PLACEMENTS** - Opportunities, eligibility, applications
4. **CAMPUS** - Events, rooms, library, facilities
5. **SUPPORT** - Requests, grievances, issues
6. **PROFILE** - Skills, projects, achievements, resume

---

## 9. STUDENT HOME (ACTION ENGINE)

Display:
- Today's classes
- Next lecture
- Attendance warnings
- Upcoming exams
- Pending assignments
- Placement deadlines
- Upcoming events
- Library reservations
- Important announcements
- Recommended actions

Each item: Information → Context → Action

---

## 10. CORE DATA ENTITIES

```
User (Base)
├── Student
├── Faculty
├── Admin
└── Alumni

Department
├── Subjects
├── Faculty
└── Students

Campus Structure
├── Building
├── Floor
├── Room (Classroom/Lab)
└── Equipment

Academic
├── Subject
├── Class
├── Timetable
├── Attendance
├── Exam
├── Assignment
└── PYQ

Event
├── Registration
├── Participant
├── Volunteer
├── Attendance
└── Feedback

Placement
├── Company
├── Role
├── Eligibility
└── Application

Student Profile
├── Skills
├── Project
├── Achievement
├── Certificate
├── Experience
└── Resume

Support
├── Request
├── Incident
├── Resolution
└── Audit

Campus Memory
├── Historical Events
├── Outcomes
├── Lessons Learned
└── Predictions
```

---

## 11. DATABASE SCHEMA (SQLite)

Core tables to be created:

- `users` - User accounts with roles
- `students` - Student profiles
- `faculty` - Faculty profiles
- `departments` - Department information
- `buildings` - Campus buildings
- `floors` - Building floors
- `rooms` - Classrooms/labs/facilities
- `subjects` - Course subjects
- `classes` - Class sections
- `timetable` - Class schedules
- `attendance` - Attendance records
- `exams` - Exam information
- `assignments` - Assignment details
- `events` - Campus events
- `registrations` - Event registrations
- `placements` - Placement opportunities
- `students_skills` - Student skills
- `projects` - Student projects
- `achievements` - Student achievements
- `requests` - Support requests
- `incidents` - Infrastructure incidents
- `notifications` - User notifications
- `audit_log` - Action audit trail

---

## 12. RAG & CHROMA DB INTEGRATION

**Use Cases:**
- College handbook semantic search
- Attendance policy Q&A
- Exam regulations
- Placement guidelines
- Library rules
- Event guidelines
- General campus knowledge

**Pipeline:**
```
Document Upload
    ↓
Parse & Clean
    ↓
Chunk
    ↓
Embed (OpenAI/Local)
    ↓
Store in Chroma DB
    ↓
Retrieve on Query
    ↓
Grounded LLM Response
```

---

## 13. API STRUCTURE (Flask)

### Authentication
- `POST /api/auth/register`
- `POST /api/auth/login`
- `POST /api/auth/logout`
- `GET /api/auth/profile`
- `PUT /api/auth/profile`

### Students
- `GET /api/students/{id}`
- `GET /api/students/{id}/academics`
- `GET /api/students/{id}/attendance`
- `GET /api/students/{id}/placements`

### Faculty
- `GET /api/faculty/{id}`
- `GET /api/faculty/{id}/classes`
- `GET /api/faculty/{id}/timetable`

### Academics
- `GET /api/academics/timetable`
- `GET /api/academics/attendance`
- `GET /api/academics/exams`
- `GET /api/academics/assignments`
- `GET /api/academics/pyqs`

### Campus
- `GET /api/campus/buildings`
- `GET /api/campus/rooms`
- `GET /api/campus/rooms/{id}/availability`
- `GET /api/campus/events`

### Events
- `POST /api/events/{id}/register`
- `GET /api/events/{id}/attendance`
- `POST /api/events/{id}/volunteer`

### Placements
- `GET /api/placements`
- `GET /api/placements/{id}/eligibility`
- `POST /api/placements/{id}/apply`

### Support
- `POST /api/requests`
- `GET /api/requests/{id}`
- `POST /api/incidents`

### Intelligence
- `GET /api/intelligence/home-actions`
- `GET /api/intelligence/impact-analysis/{entity}`
- `POST /api/intelligence/what-if`
- `GET /api/intelligence/data-health`

### RAG / Knowledge Base
- `POST /api/knowledge/upload-document`
- `POST /api/knowledge/query`
- `GET /api/knowledge/documents`

### Health
- `GET /api/health`

---

## 14. TESTING STRATEGY

**Minimum Coverage:**
- Unit tests for business logic
- Integration tests for APIs
- Component tests for React
- E2E tests for critical workflows

**Critical Test Cases:**
1. Authentication & RBAC
2. Timetable conflict detection
3. Room booking conflicts
4. Capacity violation checks
5. Attendance eligibility calculation
6. Placement eligibility matching
7. Event prediction accuracy
8. Campus impact analysis
9. Data health validation
10. Digital library configuration

---

## 15. DOCUMENTATION FILES TO MAINTAIN

- `PROJECT_PLAN.md` - This file (overall plan)
- `PROJECT_PROGRESS.md` - Weekly progress tracking
- `ARCHITECTURE.md` - System architecture details
- `API.md` - Complete API documentation
- `CHANGELOG.md` - Version history
- `DEPLOYMENT.md` - Deployment instructions
- `DATABASE.md` - Database schema details
- `README.md` - Setup and run instructions

---

## 16. DOCKER SETUP

**Services:**
```yaml
frontend:
  - React app on port 3000

backend:
  - Flask API on port 5000

sqlite:
  - SQLite database (persistent volume)

chroma:
  - Chroma DB for RAG (port 8000, persistent volume)
```

**Environment Variables:**
```
FLASK_ENV=development
DATABASE_URL=sqlite:///campus.db
CHROMA_DB_PATH=/data/chroma
OPENAI_API_KEY=xxx
JWT_SECRET=xxx
```

---

## 17. DEPLOYMENT STRATEGY

1. **Local Development** - Docker Compose on developer laptop
2. **Hackathon Machine** - Docker Compose on event machine
3. **Cloud** - AWS EC2 with Docker

Portability: Laptop → Hackathon → AWS (no code changes)

---

## 18. SUCCESS CRITERIA

### Demo Day
Student logs in → sees personalized home → checks academics → explores placements → navigates campus → sees live room availability → admin sees impact analysis

### System Health
- All P0 features working
- Authentication secure
- Database consistent
- Docker runs cleanly
- No silent failures
- Comprehensive audit trail

### User Experience
- Student feels "finally, one place for everything"
- Faculty can quickly adapt to changes
- Coordinator understands demand/capacity
- Admin sees campus-wide intelligence

---

## 19. KNOWN CONSTRAINTS & CONSIDERATIONS

1. **AI/LLM Integration** - Use Chroma for semantic search, be explicit about knowledge boundaries
2. **Human-in-Loop** - AI predicts/recommends, humans approve official actions
3. **Data Privacy** - Role-based access control, no unnecessary data storage
4. **Scalability** - Start modular monolith, can split to microservices later if needed
5. **Offline Capability** - Core features should work if external services unavailable

---

## 20. NEXT STEPS

1. **CHUNK 1 - Foundation** (First Phase)
   - Inspect repository
   - Setup Docker Compose
   - Create SQLite database structure
   - Build basic Flask backend shell
   - Build basic React frontend shell
   - Health check endpoint
   - Update documentation
   - Commit stable state

2. Then proceed to CHUNK 2 only after CHUNK 1 is complete and tested.

---

**Start Date:** 2026-09-07  
**Target Completion:** Hackathon Ready (P0 + P1)  
**Repository:** https://github.com/atuljha243/SkillSphere

---

*This plan is intentionally modular to support incremental AI-assisted development. Each chunk builds on previous work without breaking existing functionality.*
