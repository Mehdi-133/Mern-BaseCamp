# 🧪 Brief 2 Exercise Roadmap

Each exercise should take about 5 to 15 minutes and check one concept. Full feature implementation belongs in later project checkpoints.

## 🧭 Planned exercises

| Concept | Exercise | Completion evidence | Status |
| --- | --- | --- | --- |
| API takeover and non-regression | [Identify one regression](./api-takeover-non-regression.md) | Explain the idea and identify the broken behavior | 🟡 In progress |
| API contracts and errors | Choose the correct status code for three small cases | Explain each choice in one sentence | ⬜ Not started |
| Password authentication | [Predict three login results](./login-jwt-checkpoints.md), Exercise 1 | Explain why the responses differ | ⬜ Not started |
| JWT authentication | [Inspect one token payload](./login-jwt-checkpoints.md), Exercise 2 | Explain what the server must verify | ⬜ Not started |
| Roles and ownership | [Mark three requests as allow or deny](./roles-and-resource-ownership.md) | Explain the difference between role and ownership | 🟡 In progress; answers pending |
| Domain models and ordering | Choose the correct relationship or index for three rules | Explain one modeling choice | ⬜ Not started |
| Enrollment invariants | Predict what should happen when the same enrollment is requested twice | Explain why the database also needs the rule | ⬜ Not started |
| Controlled upload | [Explain the multipart-to-resource flow](./controlled-file-uploads.md) | Explain `req.file`, storage, metadata, cleanup, and merged-versus-branch evidence | ⬜ Not started |
| Sequential progress | Decide whether three module actions are allowed or locked | Explain the sequence rule | ⬜ Not started |
| Trainer reporting | Allow or deny three trainer data requests | Explain the ownership boundary | ⬜ Not started |
| Behavioral tests | [Read one Jest/Supertest example](./jest-and-supertest.md) | Explain the tools, predict a mismatch, and identify act/assert | 🟡 In progress: answers pending |
| Documentation and runtime | Find one missing or unclear restart instruction | Explain how it affects another developer | ⬜ Not started |

Detailed exercise files are created only when their concept starts. Each one stays small; broader implementation and testing are tracked separately.
