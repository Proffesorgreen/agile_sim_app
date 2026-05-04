# Branch Naming Reference — AASTU Library Agile Sim

> **Format:** `type/DT-XX-short-description-in-kebab-case`
> Branch names must match the Jira ticket they belong to.
> All lowercase. Hyphens between words. No spaces, underscores, or slashes in the description.

---

## Format Rules

```
type/DT-XX-short-description
│     │
│     └─ Jira ticket key + hyphen-separated description
└─ Branch type prefix
```

---

## Branch Types

| Prefix | When to Use |
|--------|-------------|
| `feature/` | User story implementation (most tickets) |
| `docs/` | Documentation-only changes (sprint docs, retro, standup) |
| `hotfix/` | Urgent bug fix discovered during the sprint |
| `test/` | Test files only (DT-14, DT-15) |

---

## Sprint 1 Branches

```bash
# Feature branches — one per ticket
git checkout -b feature/DT-1-member-registration
git checkout -b feature/DT-2-member-login
git checkout -b feature/DT-3-member-logout
git checkout -b feature/DT-5-book-search
git checkout -b feature/DT-6-book-detail-view
git checkout -b feature/DT-7-borrow-book
git checkout -b feature/DT-8-return-book

# Documentation branches (create from dev/main — not tied to a code ticket)
git checkout -b docs/sprint1-plan
git checkout -b docs/sprint1-review
git checkout -b docs/sprint1-retrospective

# Hotfix example (if a bug is found mid-sprint)
git checkout -b hotfix/DT-8-return-book-count-error
```

---

## Sprint 2 Branches

```bash
git checkout -b feature/DT-4-otp-password-recovery
git checkout -b feature/DT-9-librarian-add-books
git checkout -b feature/DT-10-view-all-borrowings
git checkout -b feature/DT-11-member-dashboard
git checkout -b feature/DT-12-library-analytics
git checkout -b feature/DT-13-responsive-mobile-design
git checkout -b test/DT-14-auth-unit-tests
git checkout -b test/DT-15-borrow-return-unit-tests
git checkout -b feature/DT-16-production-release-v1-1

# Documentation
git checkout -b docs/sprint2-plan
git checkout -b docs/sprint2-review
git checkout -b docs/sprint2-retrospective
```

---

## Full Ticket Workflow (per branch)

```bash
# 1. Always branch from dev (not main)
git checkout dev
git pull origin dev
git checkout -b feature/DT-7-borrow-book

# 2. Do your work and commit with ticket key
git add .
git commit -m "feat(borrow): DT-7 implement borrow endpoint with DB transaction"
git commit -m "feat(borrow): DT-7 add borrow confirmation UI and due date display"

# 3. Push branch
git push origin feature/DT-7-borrow-book

# 4. Open PR on GitHub
#    Title: "DT-7: Borrow a Book"
#    Base: dev (NOT main)
#    Fill in the PR template

# 5. Assign a reviewer, get approval, merge

# 6. Delete the feature branch after merge
git branch -d feature/DT-7-borrow-book
git push origin --delete feature/DT-7-borrow-book

# 7. Move ticket to Done in Jira
```

---

## What NOT to Do

```bash
# ❌ Branching directly from main for a feature
git checkout -b feature/DT-7-borrow-book main   # wrong — use dev

# ❌ Missing ticket key
git checkout -b borrow-feature

# ❌ Spaces or underscores
git checkout -b feature/DT_7_borrow_book
git checkout -b feature/DT-7 borrow book

# ❌ Multiple tickets in one branch
git checkout -b feature/DT-7-and-DT-8   # one branch per ticket

# ✅ Correct
git checkout -b feature/DT-7-borrow-book
```