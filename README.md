# AASTU Library Management System – Update
## Software Configuration Management (SCM) Mini Project

**Department of Software Engineering**  
**Addis Ababa Science and Technology University (AASTU)**

---

## 1. Project Overview
This project demonstrates the practical application of **Software Configuration Management (SCM)** principles using Git and GitHub. The system is an updated prototype of the AASTU Library Management System, developed primarily to showcase proper configuration control rather than programming complexity.

> **Note:** The emphasis of this project is on SCM processes such as version control, change management, baselines, releases, and audits.

---

## 2. Project Objectives
This project fulfills the following SCM objectives:
*   Prepare and apply a **Software Configuration Management Plan (SCMP)**.
*   Identify and manage **Configuration Items (CIs)**.
*   Use **Git/GitHub** for version control and branching.
*   Control changes through a formal **Change Request (CR)** process.
*   Establish **two baselines**.
*   Produce **two software releases**.
*   Conduct **Physical and Functional Configuration Audits**.
*   Prepare a final SCM project report.

---

## 3. System Scope
The system includes:
*   Login / authentication page
*   Main dashboard or menu page
*   One core functional action (e.g., borrow/return books)
*   Simple data storage
*   Frontend and backend components

---

## 4. Repository Structure
```text
.
├── docs/
│   ├── SCMP.md
│   ├── CI_Register.md
│   ├── change_requests/
│   ├── baselines/
│   ├── releases/
│   ├── audit_reports/
│   ├── SRS.pdf
│   └── Implementation.pdf
│
├── src/
│   ├── frontend/
│   └── backend/
│
├── tests/
│
├── releases/
│
└── README.md
```

## 5. Technologies Used
*   **Frontend:** Next.js, Tailwind CSS
*   **Backend:** Go (Golang), Gin Framework
*   **Version Control:** Git & GitHub
*   **Documentation:** Markdown, PDF

---

## 6. Configuration Management Approach

### Version Control Tool
*   **Git** for source control
*   **GitHub** for repository hosting, branching, pull requests, and releases

### Branching Strategy
*   `main` → stable and release-ready code
*   `dev` → integration branch
*   `feature/*` → feature development
*   `docs/*` → documentation updates
*   `hotfix/*` → urgent fixes (if required)

### Commit Message Convention
**Format:** `type(scope): short description`

*Examples:*
*   `feat(login): implement authentication page`
*   `docs(scmp): update SCM plan`
*   `fix(api): correct borrow endpoint`

---

## 7. Change Control
All changes are managed using a formal **Change Request (CR)** process. Each CR includes:
*   Description of change
*   Affected Configuration Items
*   Impact analysis
*   Approval records
*   Implementation and verification details

*CR documents are stored in:* `/docs/change_requests/`

---

## 8. Baseline Management
Two baselines are established:

**Baseline 1 (BL1)**
*   Repository structure
*   Initial documentation
*   CI Register

**Baseline 2 (BL2)**
*   Working prototype
*   Approved Change Requests implemented

**Each baseline:**
*   Is tagged in Git (`BL1`, `BL2`)
*   Has a one-page Baseline Record in `/docs/baselines/`

---

## 9. Release Management
Two releases are produced using GitHub Releases:

**Release v1.0**
*   Initial working system
*   Core features implemented

**Release v1.1**
*   Enhancements and fixes after Change Requests

*Release notes are available in:* `/docs/releases/`

---

## 10. Configuration Audits

### Physical Configuration Audit (PCA)
*   Ensures documents and Configuration Items exist
*   Verifies naming and version consistency
*   Confirms repository matches documentation

### Functional Configuration Audit (FCA)
*   Confirms approved Change Requests are implemented
*   Verifies core system functionality

*Audit reports are stored in:* `/docs/audit_reports/`

---

## 11. Team Roles and Responsibilities

| Name | Role |
| :--- | :--- |
| **Kidus Asebe** | Project Manager |
| **Kalkidan Amare** | SCM Lead |
| **Kidus Hawoltu** | Development Lead |
| **Kirubel Legese** | Frontend Developer |
| **Kirubel Wondwosen** | Backend Developer |
| **Hermela Dereje** | QA / Tester |
| **Kidus Berhane** | Documentation & Release Engineer |

---

## 12. How to Run the Project
Please refer to the respective folders for setup and execution instructions:

*   **Frontend:** See instructions inside `src/frontend/`
*   **Backend:** See instructions inside `src/backend/`

Each component contains its own README or setup guide.

---

## 13. Evidence of SCM Activities
This repository provides evidence of:
*   Multiple commits and structured history
*   Feature, documentation, and integration branches
*   Pull requests and reviews
*   Change Request documentation
*   Baseline tags (`BL1`, `BL2`)
*   GitHub Releases (`v1.0`, `v1.1`)
*   Configuration audit reports

---

## 14. Academic Integrity Statement
This project is developed strictly for academic purposes as part of the Software Configuration Management (SCM) course. All work follows SCM best practices and university guidelines.

---

## 15. Maintainers
**AASTU Software Engineering Students**  
SCM Mini Project – 2025