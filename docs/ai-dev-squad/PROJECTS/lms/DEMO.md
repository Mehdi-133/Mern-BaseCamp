# 🧪 First real team demonstration

**Date:** 28 October 2026. **Mode:** four actual delegated read-only reviews, coordinated in this chat. See [revision and context](CONTEXT.md).

## 🔵 Ayoube — requirements and coordination

The live Jira query returned zero FAL issues on the connected site. A real Jira story could not be analyzed. The following is an **uncreated proposal**, not an existing ticket:

**Send one inactivity reminder per learner per execution.**

Acceptance criteria: multiple qualifying enrollments for one learner produce at most one email attempt in a run; distinct eligible learners each receive an attempt; existing eligibility behavior stays intact; counts distinguish successful sends from attempts and delivery confirmation.

| Proposed subtask | Owner | Completion evidence |
| --- | --- | --- |
| Define learner deduplication and counter semantics | Walid | Focused readable diff and explanation |
| Cover duplicate/distinct/ineligible recipients with mocks | Annas | Executed focused tests on exact revision |
| Verify manual/scheduled integration in isolation | Walid → Annas | Controlled fixture, persisted result and non-delivery logs |
| Specify an honest execution receipt | Reda | Reviewable states/captions matching real fields |

No deadline, assignment or Jira status was changed. Implementation is pending a scoped request.

## 🟢 Walid — source-grounded engineering plan

All three jobs already exist. `services/jobHandlers.js` loops active enrollments for inactivity reminders; one learner with several enrollments can reach the email sender repeatedly. This is a **source-derived risk**, not a reproduced failure.

Proposed change: keep a `Set` of processed learner IDs within one invocation; deduplicate before expensive activity queries/email work; define whether the set records attempted or successful recipients and preserve per-recipient failure handling. Proposed scope: the reminder handler and focused tests only. A per-run set does not prevent overlapping runs or replicas.

Developer-to-QA handoff: verify one learner/two enrollments, two distinct learners, recent activity, missing/inactive learner, disabled notifications and recipient failure isolation. Review current result counters before asserting exact expected totals. Suggested future commit: `fix(jobs): deduplicate inactivity reminder recipients`.

## 🟣 Annas — evidence and test gate

**PASS — four executed syntax checks:**

```text
node --check services/jobScheduler.js
node --check services/jobHandlers.js
node --check services/jobExecutionService.js
node --check scripts/runStats.js
```

**BLOCKED / unexecuted:** HTTP, MongoDB, email, Docker, scheduler timing, CI and integration suites. These require an explicitly isolated environment; the setup did not run database-mutating tests.

No execution lock/overlap guard was found in inspected scheduling code. Concurrent manual/cron calls and replicas therefore need a defined skip/reject/queue policy if duplicate prevention is required. Refreshing schedules stops previous registrations in one process; it does not serialize executions. The cron callback uses `void runJob(...).catch(...)`; completion is not returned to the scheduler.

| Proposed test | Observable result |
| --- | --- |
| Stats fixtures / empty database | Exact counts/averages or empty arrays and zero totals |
| Handler rejection | Persisted failed execution and observable error |
| Execution record create/update failure | No false success; error remains visible |
| Schedule enabled/disabled/invalid/refresh/stop | Correct registrations and Casablanca timezone |
| Concurrent/manual/replica triggers | Approved overlap policy enforced |
| Authorization | No token 401; learner/trainer 403; admin success; unknown job 404 |
| Docker restart/database unavailable | Persistence/lifecycle behavior recorded with actual evidence |

Release recommendation: **investigate and verify before delivery**. Syntax success is not release readiness.

## 🟠 Reda — relevant design concept

**Execution receipt**, a proposed view or demonstration card: job name, execution ID, exact status, start/finish timestamps, duration when calculable, result details and failure message. Show timestamps in Africa/Casablanca.

Keep execution state (running/success/failed) separate from outcome (sent/skipped/disabled/errors when present). A successful disabled handler with `sent: 0` is not an email delivery. The inspected model does not record manual versus scheduled trigger: do not invent that label. A saved running record does not prove the process is alive.

Use navy, clear typography and named states/icons as well as role colors. Target readable normal text contrast of 4.5:1, keyboard access for any controls, 200% zoom and narrow layouts. No frontend page, native Figma design, history endpoint or video was created.

## 📬 Actual handoff result

Walid → coordinator: source baseline and narrow deduplication proposal.
Annas → coordinator: four syntax passes, isolation gate and test plan.
Reda → coordinator: execution-receipt specifications and accessibility checks.
Coordinator → Ayoube: combined findings; Ayoube returned the uncreated story and four subtasks above.

No file was edited by these reviewers. This demonstrates actual delegated analysis and saved context transfer; implementation/retest/delivery stages have not run.

## 🚀 One next step

Resolve access to the team's actual Jira site, then ask Ayoube to map one real story to this source evidence. Observable check: issue key, description, acceptance criteria and visible current status are read from the correct board before any Jira update.
