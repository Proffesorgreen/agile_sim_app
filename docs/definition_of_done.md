# Definition of Done
## Global Definition of Done (applies to every ticket)
A User Story is Done when ALL of the following are true:
### Code
- [ ] Feature fully implemented as described in the User Story
- [ ] All acceptance criteria from the Jira ticket are met
- [ ] No known bugs introduced
- [ ] No hardcoded values or debug console.log statements
### Git & GitHub
- [ ] Feature branch created from main (naming: feature/AGILE-XX-description)
- [ ] All commits reference the Jira ticket key (e.g. AGILE-5)
- [ ] Pull Request opened with completed PR template
- [ ] PR merged to main
- [ ] Feature branch deleted after merge
### Jira
- [ ] Ticket status moved to Done
- [ ] Linked PR visible in the ticket’s Development panel
### Testing
- [ ] Feature tested manually and working
- [ ] No regression in existing features
- [ ] Unit tests added (required for LIB-14, LIB-15)