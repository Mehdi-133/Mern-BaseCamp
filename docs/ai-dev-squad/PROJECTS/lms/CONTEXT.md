# 📦 LMS — audited project context

> **Source-inspected snapshot: 28 October 2026.** Refresh before implementation.

- Repository: `C:/Users/LENOVO/Desktop/fondations_API_LMS`.
- Branch: `FAL-160-b-3-openapi-documenter-les-routes-et-schemas-du-brief-3`.
- HEAD: `4041457ca89b120be7edd534d883a00666f05bdc`.
- Initial working tree: untracked `.playwright-cli/`; no tracked edits reported.
- No root AGENTS.md found in the LMS checkout during this audit.
- Stack observed in package.json: CommonJS Node/Express/Mongoose, Jest/Supertest, node-cron, Nodemailer, Swagger and Docker-related project work. Do not assume Java/Angular from the generic team brief applies to this checkout.
- Jobs already implement inactivity reminders, trainer summaries and statistics. Older BaseCamp handoffs refer to an earlier snapshot and separate practice clone.
- This setup authorizes read-only LMS inspection. It does not authorize a feature implementation, database fixture mutation or real email sends.

## 🏗️ Architecture evidence

`server.js` connects MongoDB before scheduling. `services/jobScheduler.js` registers configured jobs, uses Africa/Casablanca, and records execution through `services/jobExecutionService.js`. `services/jobHandlers.js` owns the business logic. `models/JobExecution.js` stores running/success/failed, timestamps, result and error message. `controllers/jobController.js` exposes manual execution through admin-protected job routes.

`statsRefresh` groups enrollments by course, averages progress, and counts total/active quizzes. A source implementation is present; exact results, persistence, scheduling, email and authorization behavior remain unverified by runtime tests in this setup.

## 🚧 Open boundaries

Connected Jira returned no FAL issues. Historical notes identify a different team site, `marouakourdi61.atlassian.net`; it is not in today's accessible-resource response. This is an access/context gap, not proof the backlog is empty. Do not fabricate an issue or mark a story complete.

Test setup and route tests can mutate `lms_test`. Read setup/cleanup and designate an isolated database and non-delivery email driver before runtime checks.

Full review: [demonstration](DEMO.md).
