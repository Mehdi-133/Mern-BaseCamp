# 📋 Sprint 2 — Brief 2: Authentification, accès et progression LMS

> 🟡 **In progress:** the full brief was analyzed on 2026-10-09 and verified against its official Simplonline page on 2026-10-12. The ordered concept roadmap is ready, and the existing API baseline must be verified before new implementation.

## 🔗 Official brief

- Source: [official Simplonline brief](https://maghreb.simplonline.co/classrooms/4867b8e5-eb61-4ad3-a538-a88b9ebb5957/briefs/89986592-a062-464e-bd28-b1e00fe16171), verified read-only on 2026-10-12
- Repository copy: [Brief content](./brief-content/)
- Official title: **Authentification, accès et progression LMS**
- Assignment: **Group assignment — To be submitted**
- Simplonline workspace: **Lake Titans**
- Rule: use the original brief document or official school/project page as the source of truth.

## 🤝 Team

- Work mode: **Binôme**
- Collaborators: **Mehdi and Maroua**
- Platform evidence: Simplonline confirms a group assignment; the visible workspace is named **Lake Titans**.

## 📌 Confirmed information

| Item | Current information |
| --- | --- |
| Sprint | Sprint 2 |
| Brief | Brief 2 |
| Team | Mehdi and Maroua |
| Project | Secure the existing LMS API and add the backend learning flow |
| Core stack | Node.js, Express, MongoDB, and Mongoose |
| Required security | bcrypt password hashing, JWT, private routes, roles, ownership, and safe secrets |
| Main LMS flow | Courses, ordered modules, resources, enrollments, sequential progress, and trainer views |
| Verification | Postman or Insomnia plus focused automated tests with Supertest |
| Delivery track | Jira, Git branches or forks, pull requests and reviews, API docs, README, and Docker |
| Official title | Authentification, accès et progression LMS |
| Official brief link | [Simplonline](https://maghreb.simplonline.co/classrooms/4867b8e5-eb61-4ad3-a538-a88b9ebb5957/briefs/89986592-a062-464e-bd28-b1e00fe16171) |
| Assignment status | Group assignment — To be submitted |
| Group workspace | Lake Titans |
| Authentication decision | The brief explicitly requires a learner-built JWT flow using `jsonwebtoken` and bcrypt or bcryptjs |
| Clerk investigation | Learning reference only; it is not the selected implementation for this brief |
| Learning source | ChatGPT project `ghost ai`, conversation `Clerk CLI And MCP Explained` |
| Start date | 2026-10-05 |
| Deadline | 2026-10-16 |
| Assessment | 45 to 75 minute team defense with individual questions |
| Status | 🟡 In progress |

## 🗂️ Workspace

| Area | Purpose | Status |
| --- | --- | --- |
| [Brief content](./brief-content/) | Supplied requirements and source details | ✅ Saved |
| [Brief analysis](./brief-analysis/) | Plain-language explanation, current gaps, risks, and visual roadmap | ✅ Analysis and visual pack ready |
| [Concepts](./concepts/) | Ordered technical learning roadmap | 🟡 Twelve concepts mapped; Concept 5 active by learner request; earlier Concept 1/4 checks remain open |
| [Notes](./notes/) | Brief analysis, decisions, questions, and team responsibilities | 🟡 Full intake, current-code baseline, and `jwt.verify()` review notes recorded |
| [Exercises](./exercises/) | Short understanding practice for every concept | 🟡 Concept 5 three-request exercise prepared; answers pending |

## 🧭 Concept-by-concept workflow

1. Open the next concept in the [ordered roadmap](./concepts/).
2. Learn the idea with a 5 to 15 minute prediction, explanation, or micro-task.
3. Mehdi completes the linked exercise before receiving a full correction.
4. Keep full feature implementation and broad project verification in later checkpoints.
5. Save the concept lesson and visuals only after understanding is demonstrated.
6. Update the trackers and move to the next concept only when the checkpoint is verified.

## 🛡️ Scope boundary

The concept path focuses on the JavaScript backend: Node.js, Express, Mongoose, Zod, bcrypt, JWT, Multer, API design, and JavaScript tests. Required collaboration and delivery work is tracked separately so Jira, Git review, documentation, and Docker are not forgotten or confused with programming concepts.

## 🎯 Next step

Start the agreed E08 inspection checkpoint: identify the resource's module reference and URL, then explain why a URL is not a real uploaded file. See the [14 October checkpoint](./notes/2026-10-14-brief-checkpoint.md) for mentor feedback, pair-work evidence, and workflow diagrams. Earlier roles, JWT, and non-regression exercises remain open.

## 📊 Latest evidence — 14 October

The mentor's screenshot at `cf906bd` gives **55/100 coverage**. Upload, trainer views, and tests are missing; JWT, roles, and progression are partial. This is a dated assessment, not a new runtime certification. Today's check-in chat reports PRs #22–#26 merged; those merges were not re-audited in this recap. The [checkpoint note](./notes/2026-10-14-brief-checkpoint.md) separates historical evidence, fresh source findings, and remaining verification.

## 🛡️ Current learner-selected concept — 2026-10-12

[Roles and resource ownership](./concepts/roles-and-resource-ownership/) is now the active study topic at Mehdi’s request. The lesson, review note, and visual workflow are prepared; understanding and full API behavior remain unverified. Earlier checkpoints remain open.

**Current next step:** answer the [three-request exercise](./exercises/roles-and-resource-ownership.md).
