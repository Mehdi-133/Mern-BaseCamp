# 📄 Authentification, accès et progression LMS

> ✅ **Official source verified:** the saved brief text matches the assigned Simplonline brief reviewed read-only on 2026-10-12.

- [Official Simplonline brief](https://maghreb.simplonline.co/classrooms/4867b8e5-eb61-4ad3-a538-a88b9ebb5957/briefs/89986592-a062-464e-bd28-b1e00fe16171) — assigned group brief, currently **To be submitted**.
- [Repository source copy](./source-text.md) — preserved in French and checked against the official page.
- This page is the structured reading guide for that source.

## 🎯 Project context

The LMS API already contains a catalog of courses, modules, and resources. The team must reuse a stable base, preserve the catalog, and add the core backend LMS behavior for visitors, learners, trainers, and administrators.

## 🧭 Objectives

- Take over an existing API without regression.
- Organize a two-person backlog with named tickets.
- Secure the API with password hashing, JWT, roles, and protected routes.
- Manage courses, ordered modules, resources, and controlled real uploads.
- Implement enrollments and strict sequential learner progress.
- Expose trainer endpoints.
- Test critical scenarios manually and automatically.
- Document the API and provide a reproducible runtime.

## 🔁 Transition from Brief 1

Before new development:

- Choose the technical base to reuse and keep `main` stable.
- Verify installation, MongoDB, seed data, and catalog routes.
- List preserved, changed, removed, and postponed endpoints.
- Update Jira and named tickets.
- Separate regression corrections from new features.
- Justify implementation differences from the Brief 1 UML.

## 🔐 Users, authentication, and permissions

- Provide registration, login, connected profile, password hashing, JWT, and private routes.
- Public registration always creates a `learner`; it never grants `trainer` or `admin`.
- Support `learner`, `trainer`, and `admin` roles plus account status.
- Use authentication and authorization middleware with consistent `401` and `403` responses.
- Visitors see published courses, learners see enrolled content, trainers manage their own courses, and admins supervise the platform.
- Create trainers through a seed, an admin action, or an approved request.

## 📚 Courses, modules, and resources

Mandatory behavior:

- Trainers create and update course information, publish courses, and unpublish them.
- Trainers create, update, and list ordered modules inside a course.
- Resources belong to the correct module and are accessible only when permissions allow.
- The API supports a controlled real upload for PDFs or images, or an equivalent documented sprint solution.
- Resources may represent articles, videos, external links, PDFs, or images.

Recommended after the foundation is stable:

- Archive courses, modules, and resources.
- Reorder modules and resources through simple endpoints.
- Filter trainer courses by draft, published, or archived status.

May be postponed when documented as a known limitation:

- Permanent deletion.
- Change history.
- Cloud storage.
- A complete trainer-request workflow.
- Advanced multi-trainer course management.
- Detailed statistics.

## 🎓 Enrollment and progress

- An `Enrollment` connects a learner and a course.
- A learner may follow several courses, but only one active enrollment may exist for the same learner-course pair.
- Learners can start or resume a course and mark resources as viewed.
- A module can be completed only when its completion rule is satisfied.
- The backend blocks access to or validation of a module while the previous module is incomplete.
- Module state must expose `accessible`, `locked`, `in progress`, or `completed` behavior.
- The backend calculates global progress and prevents inconsistent duplicates.
- Trainers can inspect enrolled learners and their progress in the trainer's own courses.

## 🧪 Verification

Use two levels:

1. A Postman or Insomnia collection for the main scenarios.
2. Focused automated tests with Jest and Supertest, or Vitest and Supertest when justified.

Critical scenarios include account creation, login, missing token, insufficient role, trainer ownership, enrollment, duplicate active enrollment, resource or module completion, and rejection of locked-module access.

## 🛠️ Technical constraints

| Area | Requirement |
| --- | --- |
| Stack | Node.js, Express, MongoDB, Mongoose |
| Authentication | `jsonwebtoken` and bcrypt or bcryptjs |
| Upload | Multer or a documented equivalent |
| Architecture | Separate routes, controllers, models, and middleware |
| Errors | Consistent JSON and appropriate HTTP status codes |
| Documentation | Swagger/OpenAPI or equivalent, README, and current `.env.example` |
| Docker | API Dockerfile or API plus MongoDB configuration |
| Secrets | Never commit passwords, tokens, or JWT secrets |

## 🤝 Collaboration

- Use a shared repository with an agreed branch or fork convention.
- Keep `main` stable.
- Use regular, explicit commits and one pull request for each meaningful feature or correction.
- Each teammate reviews and validates the other's pull request before merging.
- Keep individual contributions visible through tickets, branches or forks, pull requests, commits, documentation, tests, or corrections.

## 🎁 Bonus only after mandatory work

- Refresh tokens.
- More complete Zod validation.
- A progress-summary endpoint for a future React progress bar.
- S3, R2, Supabase Storage, or MinIO-compatible storage.
- Wider test coverage, structured logs, or advanced pagination.

## 📅 Dates and assessment

- Start: **2026-10-05**.
- Deadline: **2026-10-16**.
- Team: **binôme**.
- Defense: approximately **45 to 75 minutes**, with individual questions.

The presentation must cover the reused base, justified UML differences, collaboration workflow, authentication, permissions, enrollment, progress, verification, and known limitations.

## 📦 Deliverables

- Shared GitHub repository with visible pull requests and reviews.
- Jira backlog with named tickets.
- Secured API with User, Enrollment, progress, authentication, authorization, and real upload behavior.
- Documented course, module, and resource endpoints.
- Postman or Insomnia collection plus focused automated tests.
- README, API documentation, and current `.env.example`.
- Docker API or API plus MongoDB configuration.

## ✅ Performance criteria

- The existing catalog does not regress.
- Passwords are hashed, JWT access is verified, roles are limited, and errors do not leak sensitive information.
- Trainers can build usable courses with ordered modules and correctly linked resources.
- Enrollment remains coherent and sequential progress is enforced by the backend.
- Critical scenarios are repeatable and tested.
- Pull requests and reviews show both teammates' contributions.
- The README restarts the project and lists known limitations.
