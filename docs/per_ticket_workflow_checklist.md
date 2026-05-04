# Per-Ticket Workflow Checklist

> Copy this checklist into a comment on the Jira ticket when you start work.
> Check each item off as you go. The ticket is not Done until every box is ticked.

---

## Template (copy into Jira ticket comment)

```
## Ticket Workflow Checklist

### Jira
- [ ] Ticket moved to **In Progress** on the Active Sprint board
- [ ] Acceptance criteria read and understood before writing any code
- [ ] Ticket assigned to the correct team member

### GitHub — Setup
- [ ] Pulled latest `dev` branch before creating feature branch
- [ ] Feature branch created: `feature/LIB-XX-short-description`
- [ ] Branch pushed to remote

### GitHub — Development
- [ ] All commits include ticket key: `LIB-XX` in the message
- [ ] Commit messages follow format: `type(scope): LIB-XX description`
- [ ] No debug `console.log` or hardcoded values left in code
- [ ] Feature tested locally — works as expected

### GitHub — Pull Request
- [ ] PR opened with title: `LIB-XX: Story Title`
- [ ] Base branch set to `dev` (NOT `main`)
- [ ] PR template fully filled in (all sections completed)
- [ ] Reviewer tagged in the PR (`@teammate`)
- [ ] All acceptance criteria checked off in the PR template
- [ ] Screenshots attached (if UI change)

### Code Review
- [ ] Reviewer has approved the PR
- [ ] Reviewer comments addressed (if any)

### Merge & Cleanup
- [ ] PR merged to `dev`
- [ ] Feature branch deleted (remote + local)
- [ ] No merge conflicts left in `dev`

### Jira — Close
- [ ] Ticket moved to **Done** in Jira
- [ ] Linked PR visible in the ticket's Development panel (GitHub for Jira)
- [ ] STANDUP.md updated to reflect completion

### Definition of Done — Final Check
- [ ] Feature fully works as described in the user story
- [ ] All acceptance criteria from the ticket are satisfied
- [ ] No regressions in existing features
- [ ] No console errors or test failures
```

---

## Filled Example — LIB-7 (Borrow a Book)

```
## Ticket Workflow Checklist — LIB-7

### Jira
- [x] Ticket moved to In Progress on the Active Sprint board
- [x] Acceptance criteria read: availability check, due date = +14 days, copy count decrements
- [x] Assigned to: [Name]

### GitHub — Setup
- [x] Pulled latest dev: git pull origin dev
- [x] Branch created: feature/LIB-7-borrow-book
- [x] Branch pushed to remote

### GitHub — Development
- [x] Commits:
      feat(borrow): LIB-7 implement borrow endpoint with DB transaction
      feat(borrow): LIB-7 add borrow confirmation UI and due date display
- [x] No console.log or hardcoded values
- [x] Tested: borrow works, copy count decrements, due date is correct

### GitHub — Pull Request
- [x] PR: "LIB-7: Borrow a Book"
- [x] Base: dev
- [x] PR template filled in
- [x] Reviewer: @[teammate]
- [x] ACs checked: availability check ✅, due date ✅, count decrement ✅
- [x] Screenshots: borrow confirmation modal attached

### Code Review
- [x] Approved by @[teammate]
- [x] Fixed: reviewer noted missing error state for 0-copies — added

### Merge & Cleanup
- [x] Merged to dev
- [x] Branch deleted
- [x] dev clean

### Jira — Close
- [x] Moved to Done
- [x] PR visible in Development panel
- [x] STANDUP.md updated: "Day 6 — LIB-7 borrow book merged"

### Definition of Done — Final Check
- [x] Borrow feature works end-to-end
- [x] All 3 ACs satisfied
- [x] Existing auth and search still working
- [x] No errors in console

```
