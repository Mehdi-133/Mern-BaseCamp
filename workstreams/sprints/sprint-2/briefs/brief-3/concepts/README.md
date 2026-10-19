# 🧠 Brief 3 Concept Roadmap

> 🟡 Study one concept at a time. These roadmap rows are preparation, not proof of understanding or implementation.

## 🧭 Dependency-based order

| # | Concept | Exact brief connection | Short check | Status |
| ---: | --- | --- | --- | --- |
| 1 | Stable baseline and non-regression | Stabilize `main`; verify every Brief 2 flow before new work | Build a pass/fail/unknown baseline matrix | ⬜ Not started |
| 2 | API contract for React | Stable endpoints, demo data, predictable errors, documented contract | Compare one success and two error response shapes | ⬜ Not started |
| 3 | Quiz domain modeling and safe projections | Module quiz, choices, secret correct answers, activation, threshold, required/optional | Mark fields as public, trainer-only, or server-only | ⬜ Not started |
| 4 | Backend scoring and attempt state | Server-calculated score, saved answers, date, status, result | Calculate one attempt by hand and name trusted inputs | ⬜ Not started |
| 5 | Progression gates as explicit rules | Required pass unlocks; optional failure does not block | Predict three unlock decisions | ⬜ Not started |
| 6 | Feedback authorization and ownership | Trainer owns course; admin global; learner reads own feedback | Allow or deny three feedback requests | ⬜ Not started |
| 7 | Email service boundaries and templates | Five email events, two HTML templates, dynamic data, `log` mode | Separate event, template data, provider, and secret | ⬜ Not started |
| 8 | Application settings versus environment secrets | Protected admin CRUD, trainer preferences, thresholds, provider mode | Sort six values into database or environment | ⬜ Not started |
| 9 | Scheduled jobs, idempotency, and run history | Configurable jobs, manual trigger, traceable executions | Design one repeat-safe inactive reminder key | ⬜ Not started; PDF details missing |
| 10 | Statistics and scoped aggregation | React-ready stats and trainer-only course data | Define one statistic with input, filter, and JSON output | ⬜ Not started |
| 11 | Behavioral tests and side-effect isolation | Targeted automated tests and executable API collection | Identify arrange, act, assert, and fake dependency | ⬜ Not started |
| 12 | OpenAPI, demo seed, Docker, and delivery evidence | Reproducible launch, docs, contract, PRs, reviews, contributions | Audit one fresh-clone path from README to response | ⬜ Not started |

## 📚 Book bridge

- Objects and arrays support the domain data in concepts 3–5.
- Higher-order functions support scoring and statistics in concepts 4 and 10.
- Bugs and Errors supports baseline checks, predictable failures, and tests.
- Modules supports clean boundaries between scoring, email, jobs, and HTTP controllers.
- Asynchronous Programming supports database, SMTP, and scheduled work.
- HTTP and Node.js support the React contract and reproducible API behavior.

Detailed lesson folders are created only when a concept study begins.
