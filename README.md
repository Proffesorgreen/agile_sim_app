# AASTU library Management System

> **Agile Project Management Simulation**  
> Department of Software Engineering — Addis Ababa Science and Technology University (AASTU)

---

## 1. Project Overview

This repository demonstrates the practical application of **Agile Project Management** principles using **Jira** and **GitHub**. The system is the AASTU library Management System — a platform that allows students to register, search for books, borrow and return them, and view their borrowing history. librarians can manage the book catalogue, monitor active borrowings and overdue items, and access library usage analytics.

The project is built and managed using the **Scrum** framework across two 2-week sprints, with a full backlog, sprint planning, daily standups, sprint reviews, and retrospectives simulated throughout.

> **Note:** The emphasis of this project is on Agile processes — sprint planning, backlog management, feature branching, pull request reviews, and iterative releases — rather than programming complexity.

---

## 2. Project Objectives

This project fulfils the following Agile PM objectives:

- Define and manage a **Product Backlog** with Epics, User Stories, and Story Points
- Plan and execute **two Scrum Sprints** with clear Sprint Goals
- Apply a disciplined **Git branching strategy** (one feature branch per Jira ticket)
- Use **Pull Requests with peer review** as the merge gate for all code changes
- Integrate **Jira with GitHub** so commits and PRs are linked to tickets automatically
- Conduct and document all **Scrum ceremonies** — Planning, Standup, Review, Retrospective
- Produce **two GitHub Releases** (v1.0.0 and v1.1.0) with structured changelogs
- Maintain a live **STANDUP.md** log throughout both sprints

---

## 3. System Scope

The AASTU library Management System includes:

- Member registration and authentication (login, logout, OTP password recovery)
- Book search by title, author, or ISBN
- Book detail view with availability and copy count
- Borrow and return book workflow with due date tracking
- librarian tools: add books to catalogue, view all active borrowings and overdue items
- Member dashboard showing current borrowings and due dates
- library analytics: most borrowed books and peak usage times
- Responsive design for desktop and mobile

---

## 4. Repository Structure

```
.
├── .github/
│   ├── PULL_REQUEST_TEMPLATE/
│   │   └── pull_request_template.md   # Enforces ticket linking on every PR
│   └── CODEOWNERS                     # Auto-assigns reviewers by module
│
├── docs/
│   ├── agile_plan.md                  # Agile process plan (replaces SCMP)
│   ├── definition_of_done.md          # Global Definition of Done
│   ├── TEAM_AGREEMENTS.md             # Team working agreements
│   ├── sprint_plans/
│   │   ├── sprint1_plan.md
│   │   ├── sprint1_review.md
│   │   ├── sprint2_plan.md
│   │   └── sprint2_review.md
│   ├── retrospectives/
│   │   ├── sprint1_retro.md
│   │   └── sprint2_retro.md
│   ├── standup_logs/
│   │   ├── sprint1_standups.md
│   │   └── sprint2_standups.md
│   └── release_notes/
│       ├── v1.0.md
│       └── v1.1.md
│
├── src/
│   ├── frontend/                      # Next.js + Tailwind CSS
│   └── backend/                       # Go (Golang) + Gin Framework
│
├── tests/                             # Unit test files
│
├── releases/                          # Release artefacts
│
├── STANDUP.md                         # Running daily standup log
└── README.md
```

---

## 5. Technologies Used

| Layer | Technology |
|---|---|
| Frontend | Next.js, Tailwind CSS |
| Backend | Go (Golang), Gin Framework |
| Database | PostgreSQL |
| Version Control | Git & GitHub |
| Project Management | Jira (Scrum) |
| Jira–GitHub Integration | GitHub for Jira (Atlassian Marketplace) |
| Documentation | Markdown |

---

## 6. Agile & Git Workflow

### Scrum Framework

This project follows the Scrum framework with two 2-week sprints:

| Sprint | Goal | Story Points | Duration |
|---|---|---|---|
| Sprint 1 | Member can register, log in, search books, borrow and return | 16 pts | 2 weeks |
| Sprint 2 | OTP recovery, DTrarian tools, analytics dashboard, tests, release | 24 pts | 2 weeks |

### Branching Strategy

| Branch Type | Pattern | Purpose |
|---|---|---|
| `main` | `main` | Stable and release-ready — never commit directly |
| Feature | `feature/DT-XX-short-description` | One branch per Jira ticket |
| Docs | `docs/DT-description` | Documentation-only updates |
| Hotfix | `hotfix/DT-XX-description` | Urgent fixes on released code |

### Commit Message Convention

**Format:** `type(scope): DT-XX short description`

| Type | When to Use | Example |
|---|---|---|
| `feat` | New feature (user story) | `feat(auth): DT-1 add member registration form` |
| `fix` | Bug fix | `fix(books): DT-8 correct copy count on return` |
| `test` | Tests added or updated | `test(auth): DT-14 add unit tests for login` |
| `docs` | Documentation only | `docs(retro): add Sprint 1 retrospective` |
| `style` | UI / CSS only | `style(dashboard): DT-13 apply responsive layout` |
| `chore` | Config / setup | `chore(repo): add .gitignore` |

### Pull Request Rules

- Every Jira ticket gets **one feature branch** and **one PR**
- PRs must reference the Jira ticket: `Closes DT-XX`
- PRs require **at least one peer review approval** before merging
- Authors may **not** approve their own PRs
- Branch is **deleted** after merge

---

## 7. Jira Backlog & Sprint Management

**Jira Project:** AASTU library Agile Sim (`DT`)  
**Jira URL:** `[https://ermiasyohannes262.atlassian.net/]`  
**Integration:** GitHub for Jira — commits, branches, and PRs auto-link to tickets

### Epics

| Epic | Tickets | Colour |
|---|---|---|
| Member Authentication | DT-1 → DT-4 | 🔴 Red |
| Book & Borrowing Management | DT-5 → DT-10 | 🔵 Blue |
| Dashboard & Analytics | DT-11 → DT-13 | 🟢 Green |
| Testing & Release | DT-14 → DT-16 | 🟣 Purple |

### Full Backlog

| Ticket | User Story | Epic | Points | Sprint |
|---|---|---|---|---|
| DT-1 | As a new member I want to register with my student ID and email so I can access the DTrary | Member Auth | 3 | Sprint 1 |
| DT-2 | As a registered member I want to log in so I can borrow and return books | Member Auth | 2 | Sprint 1 |
| DT-3 | As a logged-in member I want to log out so my session stays secure | Member Auth | 1 | Sprint 1 |
| DT-4 | As a member I want OTP-based password recovery so I can regain access | Member Auth | 3 | Sprint 2 |
| DT-5 | As a member I want to search for books by title, author, or ISBN | Book & Borrow | 3 | Sprint 1 |
| DT-6 | As a member I want to view book details and availability so I know if I can borrow | Book & Borrow | 2 | Sprint 1 |
| DT-7 | As a member I want to borrow an available book so I can take it home | Book & Borrow | 3 | Sprint 1 |
| DT-8 | As a member I want to return a borrowed book so my record is updated | Book & Borrow | 2 | Sprint 1 |
| DT-9 | As a librarian I want to add new books to the catalogue | Book & Borrow | 2 | Sprint 2 |
| DT-10 | As a librarian I want to view all active borrowings and overdue items | Book & Borrow | 3 | Sprint 2 |
| DT-11 | As a member I want a dashboard showing my borrowings and due dates | Dashboard | 3 | Sprint 2 |
| DT-12 | As a librarian I want analytics showing most borrowed books and peak usage | Dashboard | 3 | Sprint 2 |
| DT-13 | As a user I want the system to be responsive on desktop and mobile | Dashboard | 2 | Sprint 2 |
| DT-14 | As a developer I want unit tests for the auth module to catch regressions | Testing | 3 | Sprint 2 |
| DT-15 | As a developer I want unit tests for borrow and return endpoints | Testing | 3 | Sprint 2 |
| DT-16 | As a product owner I want a production release v1.1 with a full changelog | Testing | 2 | Sprint 2 |

---

## 8. Sprint Milestones & Release Tags

| Milestone | Git Tag | Description |
|---|---|---|
| Sprint 1 Complete | `SPRINT1-COMPLETE` | All 16 Sprint 1 story points delivered |
| Sprint 2 Complete | `SPRINT2-COMPLETE` | All 24 Sprint 2 story points delivered |
| Initial Release | `v1.0.0` | Core DTrary system: auth + borrow/return |
| Full Release | `v1.1.0` | OTP recovery, analytics, DTrarian tools |

---

## 9. Release Management

Two releases are produced using GitHub Releases:

### Release v1.0.0 — Core DTrary System
- Member registration, login, and logout (DT-1, DT-2, DT-3)
- Book search, detail view, borrow, and return (DT-5, DT-6, DT-7, DT-8)

*Full release notes: [`docs/release_notes/v1.0.md`](docs/release_notes/v1.0.md)*

### Release v1.1.0 — OTP Recovery & DTrary Analytics
- OTP-based password recovery (DT-4)
- librarian tools: add books, view borrowings (DT-9, DT-10)
- Member dashboard and DTrary analytics (DT-11, DT-12)
- Responsive design and unit test suite (DT-13, DT-14, DT-15)

*Full release notes: [`docs/release_notes/v1.1.md`](docs/release_notes/v1.1.md)*

---

## 10. Scrum Ceremonies

### Sprint Planning
Held at the start of each sprint. The Product Owner presents the sprint goal and proposes stories. The team estimates, negotiates scope, and commits to a sprint backlog. Sprint goal and assignments are recorded in `docs/sprint_plans/`.

### Daily Standup
Held every working day. Each member answers:
1. What did I complete since the last standup?
2. What will I work on today?
3. Do I have any blockers?

### Sprint Review
Held at the end of each sprint. Each team member demos their completed stories live. The Product Owner accepts or rejects each story against its acceptance criteria. Outcomes are recorded in `docs/sprint_plans/sprintX_review.md`.

### Sprint Retrospective
Held after the Sprint Review. The team reflects using Start / Stop / Continue format and commits to 1–2 concrete process improvements for the next sprint. Outcomes are recorded in `docs/retrospectives/sprintX_retro.md`.

---

## 11. Team

| Role | Member | GitHub Username | Jira Role |
|---|---|---|---|
| Product Owner | Kirubel Legese | Administrator |
| Scrum Master | Kidus Asebe | Administrator |
| Developer 1 | Kalkidan Amare | Member |
| Developer 2 | Kidus Hawoltu | Member |
| Developer 3 | Hermela Dereje | Member |
| Developer 4 | Kidus Berhane | Member |
| Developer 5 | Kirubel Wondowossen | Member |

### Role Responsibilities

**Product Owner** — owns the backlog, writes and accepts user stories, has final say on Definition of Done. 

**Scrum Master** — facilitates all ceremonies, removes blockers, maintains STANDUP.md, monitors burndown.

**Developers** — full development team member, reviews PRs.

---

## 12. How to Run the Project

### Backend (Go + Gin)

```bash
cd src/backend
go mod tidy
go run main.go
# Server starts at http://localhost:8080
```

### Frontend (Next.js)

```bash
cd src/frontend
npm install
npm run dev
# App starts at http://localhost:3000
```

### Tests

```bash
cd tests
go test ./...
```

> See individual README files inside `src/frontend/` and `src/backend/` for full environment setup instructions.

---

## 13. Evidence of Agile Activities

| Evidence | Location |
|---|---|
| Product Backlog (16 stories, 4 epics) | Jira → Backlog view |
| Sprint 1 board — all Done | Jira → Reports → Sprint Report |
| Sprint 2 board — all Done | Jira → Reports → Sprint Report |
| Burndown Chart — Sprint 1 | Jira → Reports → Burndown Chart |
| Burndown Chart — Sprint 2 | Jira → Reports → Burndown Chart |
| Velocity Chart | Jira → Reports → Velocity Chart |
| Jira ticket with linked GitHub PR | Any DT-XX ticket → Development panel |
| 16 closed Pull Requests (one per ticket) | GitHub → Pull Requests → Closed |
| Commit history with DT-XX ticket keys | GitHub → Commits |
| Feature branch per ticket | GitHub → Insights → Network |
| Sprint 1 plan & review | [`docs/sprint_plans/`](docs/sprint_plans/) |
| Sprint 2 plan & review | [`docs/sprint_plans/`](docs/sprint_plans/) |
| Sprint 1 retrospective | [`docs/retrospectives/sprint1_retro.md`](docs/retrospectives/sprint1_retro.md) |
| Sprint 2 retrospective | [`docs/retrospectives/sprint2_retro.md`](docs/retrospectives/sprint2_retro.md) |
| GitHub Release v1.0.0 | GitHub → Releases → v1.0.0 |
| GitHub Release v1.1.0 | GitHub → Releases → v1.1.0 |
| Sprint milestone tags | GitHub → Tags → SPRINT1-COMPLETE, SPRINT2-COMPLETE |

---

## 14. Academic Integrity Statement

This project is developed strictly for academic purposes as part of the Agile Project Management course. All work follows Scrum best practices and university guidelines.

---

## 15. Maintainers

**AASTU Software Engineering Students**  
Agile Project Management Simulation — 2026