## v1.0.0 — Core Library System
**Release Date:** 05/04/2026
**Sprint:** Sprint 1 completion
### Features
- Member registration with student ID and email validation (DT-1)
- Secure member login with JWT session management (DT-2)
- Member logout and session clearing (DT-3)
- Book search by title, author, or ISBN (DT-5)
- Book detail view with availability and copy count (DT-6)
- Borrow a book with availability check (DT-7)
- Return a borrowed book with record update (DT-8)
### Technical
- Frontend: Next.js with Tailwind CSS
- Backend: Go with Gin framework
- Authentication: JWT tokens
- Database: PostgreSQL
### Known Limitations
- No OTP password recovery yet (planned for v1.1)
- Librarian book management not yet available (planned for v1.1)
- Library analytics dashboard not yet available (planned for v1.1)