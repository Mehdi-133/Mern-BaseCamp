# 🧠 Brief 2 Concept Roadmap

> 🟡 **Rule:** study one concept at a time. A roadmap entry becomes complete only after Mehdi explains it, completes its exercise, and verifies the required behavior.

## 🧭 Required learning order

| # | Concept | Why the brief needs it | Focused exercise | Review note | Current status |
| ---: | --- | --- | --- | --- | --- |
| 1 | API takeover and non-regression | New work must preserve the existing catalog and start from a stable base | [Identify one regression](../exercises/api-takeover-non-regression.md) | Created after the understanding check | 🟡 In progress: short scenario is next |
| 2 | API contracts, validation, and error flow | Every endpoint needs validated input, consistent JSON, and correct HTTP status codes | Choose status codes for three cases | [Express and Zod validation](../notes/zod-validation-middleware.md) | ⬜ Not started |
| 3 | Password authentication and account state | Login must compare a hash safely and reject suspended accounts without leaking details | [Predict three login results](../exercises/login-jwt-checkpoints.md), Exercise 1 | Created when the concept study resumes | 🟡 In progress: code exists; understanding check pending |
| 4 | JWT identity and authentication middleware | Private routes need a verified Bearer token and a trusted user identity | [Find the unsafe token claim](../exercises/login-jwt-checkpoints.md), Exercise 2 | [JWT authentication](../notes/jwt-authentication.md) | 🔁 Middleware token checks passed; [lesson review](./jwt-authentication/) and protected-route check pending |
| 5 | [Role authorization and resource ownership](./roles-and-resource-ownership/) | Learners, trainers, and admins have different rights; trainers are limited to their own courses | [Allow or deny three requests](../exercises/roles-and-resource-ownership.md) | [Quick review](../notes/roles-and-resource-ownership.md) | 🟡 In progress: learner selected this concept; explanation and HTTP checks pending |
| 6 | LMS domain modeling, relationships, and ordering | Courses, modules, resources, ownership, status, and order must stay coherent | Choose one relationship and one index | [Mongoose core concepts](../notes/mongoose-core-concepts.md) | 🔁 Review needed: partial models exist |
| 7 | Enrollment invariants and database uniqueness | One learner may join many courses but only one active enrollment per learner-course pair is allowed | Predict one duplicate-enrollment result | Created when study resumes | 🔁 Review needed: controller exists; invariant is not enforced by the database |
| 8 | Controlled file uploads and access | Real PDF/image uploads must be constrained, linked to a module, and served only to authorized users | Accept or reject three sample files | Created when study starts | ⬜ Not started |
| 9 | Sequential progress as a state machine | The backend must lock later modules, prevent invalid duplicates, and calculate progress | Decide whether three actions are locked | Created when study starts | ⬜ Not started |
| 10 | Trainer reporting and scoped queries | Trainers need learner progress without seeing another trainer's course data | Allow or deny three data requests | Created when study starts | ⬜ Not started |
| 11 | Behavioral API testing | Critical security and progress rules must be repeatable in Supertest and Postman or Insomnia | Identify arrange, act, and assert in one test | Created when study starts | ⬜ Not started |
| 12 | API documentation and reproducible runtime | Reviewers must be able to understand and restart the API safely | Find one unclear restart instruction | Created when study resumes | 🟡 In progress: partial Swagger, environment, and Docker setup exist |

## 🛠️ Delivery track

These are required sprint practices, not substitutes for the concepts above:

- Keep `main` stable and separate regressions from new features.
- Maintain named Jira tickets and an explicit responsibility split for Mehdi and Maroua.
- Use focused branches or forks, clear commits, one meaningful pull request per change, and teammate review.
- Keep the README, API documentation, known limitations, and individual contributions current.

## 📚 Book foundations

The local *Eloquent JavaScript* book supports this roadmap with:

- Chapter 6: interfaces and encapsulation for clear model and module responsibilities.
- Chapter 8: debugging, error propagation, and deliberate failure handling.
- Chapter 10: explicit module interfaces and dependencies.
- Chapter 11: asynchronous network, database, and file operations.
- Chapter 18: HTTP methods, headers, responses, and status-code families.
- Chapter 20: Node.js servers, filesystem work, streams, errors, and idempotent HTTP behavior.

Framework rules such as JWT verification, Mongoose indexes, Multer limits, Supertest, Swagger, and Docker must be learned from the brief, the installed libraries, and verified project behavior.

## 💡 Existing reference

[Clerk authentication tools](./clerk-authentication/) remains a useful comparison lesson, but Clerk is not part of the selected implementation because this brief explicitly requires the custom JWT path.
