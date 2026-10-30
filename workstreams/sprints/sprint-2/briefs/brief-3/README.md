# 🚀 Sprint 2 — Brief 3: Final LMS API Delivery

> 🟡 **In progress:** source saved; isolated Postman journeys verified on 30 October. Learner understanding, Docker replay and final reviewed delivery remain pending.

## 🎯 Mission

Deliver a stable LMS backend for the next React sprint with module quizzes, backend scoring, trainer feedback, configurable email notifications, scheduled jobs, useful statistics, predictable API contracts, tests, documentation, demo data, and Docker Compose.

## 📅 Confirmed frame

| Item | Confirmed information |
| --- | --- |
| Start | 19 October 2026 |
| Deadline | 30 October 2026 |
| Duration | 12 calendar days, including both dates |
| Work mode | Squad |
| Assessment | 30–45 minute squad defense with individual questions |
| React dependency | Stable endpoints, demo data, predictable errors, statistics, and a clear contract |

## 🧭 Workspace

- [Official source copy](./brief-content/)
- [Beginner-friendly analysis](./brief-analysis/)
- [Ordered concept roadmap](./concepts/)
- [Short understanding exercises](./exercises/)
- [Decisions, questions, and evidence boundaries](./notes/)

## 🗺️ Delivery route

1. Stabilize the inherited Brief 2 API and record regressions.
2. Agree on one API response and error contract for React.
3. Add quiz, attempt, scoring, progression, and feedback behavior.
4. Add email delivery, protected configuration, preferences, and scheduled jobs.
5. Expose scoped statistics without leaking private data or quiz answers.
6. Prove the API through tests, Postman/Insomnia, OpenAPI, seed data, Docker, PRs, and named contributions.

## 🚦 Honest status

| Area | Status |
| --- | --- |
| Source text and schedule | ✅ Saved |
| Missing PDF continuation | 🔁 Needed before job rules are final |
| Current LMS source inventory | 🟡 Read-only inspection complete; runtime baseline pending |
| Concept and exercise roadmaps | ✅ Prepared; all learning checks remain not started |
| Scheduled-jobs live coding | 🟡 `#82875` confirmed for 26 October at 14:30; preparation plan not started |
| Brief 3 application features | ⬜ Not started or not verified in this intake |
| Squad members and responsibility split | ⬜ Not confirmed by supplied text |

## 🎯 Current mission

The [FAL-163 handoff](./notes/postman-frontend-handoff.md) passed an isolated **90-request / 209-assertion** Newman run with zero failures/skips. The learner's Docker logs now report startup; successful learner replay remains pending. Use the [terminal revision notes](./notes/README.md) and [Brief 3 checklist](./notes/brief-3-delivery-revision.md).

**Source correction:** the missing required email journey is forgotten password, not quiz completion. A local test run does not establish all brief requirements or reviewed delivery.

**Ready check:** run public smoke against Docker and record four requests/eleven assertions without failures or skips, then role login/profile. Concept mastery remains unverified.
