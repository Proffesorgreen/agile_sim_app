# Commit Message Reference — AASTU DTrary Agile Sim

> **Format:** `type(scope): DT-XX short description`
> Every commit must include the Jira ticket key. This is what creates the link
> between GitHub commits and Jira tickets in the Development panel.

---

## Format Rules

```
type(scope): DT-XX short description in lowercase
│     │       │
│     │       └─ Jira ticket key — REQUIRED on every commit
│     └─ The module or area of the codebase affected
└─ The kind of change (see types below)
```

**Rules:**
- All lowercase after the colon
- No period at the end
- Keep under 72 characters total
- Use imperative mood: "add", "implement", "fix" — not "added" or "adding"

---

## Types

| Type | When to Use |
|------|-------------|
| `feat` | New feature or user-facing functionality |
| `fix` | Bug fix |
| `test` | Adding or updating tests |
| `docs` | Documentation only (README, sprint docs, retro) |
| `style` | UI/CSS changes, no logic change |
| `chore` | Config, tooling, repo setup — no production code |
| `refactor` | Code restructure with no behaviour change |

---

## Scopes

| Scope | Covers |
|-------|--------|
| `auth` | Registration, login, logout, OTP |
| `books` | Search, detail, catalogue management |
| `borrow` | Borrow and return |
| `dashboard` | Member dashboard |
| `analytics` | DTrary analytics |
| `ui` | Responsive / mobile layout |
| `tests` | Test files |
| `release` | Release prep, changelogs |
| `repo` | Repo setup, .gitignore, folder structure |
| `retro` | Retrospective docs |
| `sprint` | Sprint plan or review docs |
| `standup` | STANDUP.md updates |

---

## Examples — Sprint 1

```bash
# DT-1: Member registration
git commit -m "feat(auth): DT-1 add registration form with student ID validation"
git commit -m "feat(auth): DT-1 add backend registration endpoint and duplicate check"

# DT-2: Member login
git commit -m "feat(auth): DT-2 implement JWT login endpoint"
git commit -m "feat(auth): DT-2 add login form and connect to JWT backend"

# DT-3: Member logout
git commit -m "feat(auth): DT-3 implement logout and session clearing"

# DT-5: Book search
git commit -m "feat(books): DT-5 add book search endpoint by title, author, and ISBN"
git commit -m "feat(books): DT-5 build search UI with results list"

# DT-6: Book detail view
git commit -m "feat(books): DT-6 add book detail page with availability and copy count"

# DT-7: Borrow a book
git commit -m "feat(borrow): DT-7 implement borrow endpoint with DB transaction"
git commit -m "feat(borrow): DT-7 add borrow confirmation UI and due date display"
git commit -m "fix(borrow): DT-7 correct availability check race condition"

# DT-8: Return a book
git commit -m "feat(borrow): DT-8 implement return endpoint and update copy count"
git commit -m "fix(borrow): DT-8 correct copy count not decrementing on return"

# Docs and chores
git commit -m "docs(sprint): add Sprint 1 plan to docs/sprint_plans"
git commit -m "docs(retro): add Sprint 1 retrospective notes"
git commit -m "docs(standup): update STANDUP.md for Sprint 1 Day 3"
git commit -m "chore(repo): add .gitignore for Node, Go, and macOS artefacts"
git commit -m "chore(repo): initialise folder structure and STANDUP.md"
```

---

## Examples — Sprint 2

```bash
# DT-4: OTP recovery
git commit -m "feat(auth): DT-4 implement OTP generation and email dispatch"
git commit -m "feat(auth): DT-4 add OTP verification and password reset form"

# DT-9: librarian adds books
git commit -m "feat(books): DT-9 add new book endpoint with catalogue validation"

# DT-10: View all borrowings
git commit -m "feat(borrow): DT-10 add librarian borrowings overview with overdue filter"

# DT-11: Member dashboard
git commit -m "feat(dashboard): DT-11 build member dashboard with borrowings and due dates"

# DT-12: Analytics
git commit -m "feat(analytics): DT-12 add most borrowed books query and chart"
git commit -m "feat(analytics): DT-12 add peak usage time analytics endpoint"

# DT-13: Responsive design
git commit -m "style(ui): DT-13 make navigation responsive for mobile viewports"
git commit -m "style(ui): DT-13 fix borrow and return pages on small screens"

# DT-14 & 15: Tests
git commit -m "test(auth): DT-14 add unit tests for registration and login endpoints"
git commit -m "test(borrow): DT-15 add unit tests for borrow and return endpoints"

# DT-16: Release
git commit -m "chore(release): DT-16 update release notes for v1.1.0"
```

---

## What NOT to Do

```bash
# ❌ No ticket key
git commit -m "fix bug in borrow"

# ❌ Past tense
git commit -m "feat(auth): DT-1 added registration form"

# ❌ Vague scope
git commit -m "feat(misc): DT-5 stuff"

# ❌ Too long
git commit -m "feat(auth): DT-2 implement the JWT-based login system for the member authentication flow with session management"

# ✅ Correct
git commit -m "feat(auth): DT-2 implement JWT login with session management"
```