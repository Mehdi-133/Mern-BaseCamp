# ⏰ Automation proposals — inactive

> ⬜ No automation created. Exact schedule/trigger, scope, tools and recipients require owner approval. Search existing automations before creation to avoid duplicates.

| Workflow | Proposed scope | Needed decision |
| --- | --- | --- |
| Morning briefing — Ayoube | Authorized Jira issues, primary calendar, priorities and blockers | Days/time in Africa/Casablanca, Jira project and delivery chat |
| End-of-day check-in — Ayoube | Verified Git/test/Jira changes and unfinished work | Days/time, repository scope and delivery chat |
| Weekly review — Ayoube + Annas | Completed/incomplete acceptance criteria and recurring blockers | Weekday/time and reporting period |
| Release review — Annas | Authorized PR/CI read-only assessment | Repository, exact supported trigger and delivery chat |

Choose local execution only if the connected computer will be available. For laptop-off work, prefer a supported cloud task after verifying its access to required sources. Local repositories are not automatically accessible from cloud work.

Do not infer a supported release webhook from available recurring scheduling tools. A monitor stays quiet while unchanged/non-actionable and notifies only on a meaningful change, completion, failure or required owner action. No emails, Slack messages or external recipients without explicit authorization.
