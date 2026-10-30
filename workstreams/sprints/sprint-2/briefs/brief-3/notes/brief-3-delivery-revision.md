# 📋 Brief 3: what to revise before delivery

> 🟡 **Revision checklist — 30 October 2026.** This maps the supplied brief to concepts; it does not certify the whole project or learner mastery.

Start with the [official saved brief](../brief-content/source-text.md), [concept roadmap](../concepts/README.md) and [understanding exercises](../exercises/README.md). The supplied source still omits the continuation of section 6; do not invent its detailed job rules. Learner reports the deadline as 30 October at 16:00 Africa/Casablanca; the saved source confirms the date only.

| Requirement | Concepts to explain | Evidence to show |
| --- | --- | --- |
| Stable shared baseline | Branch, commit, regression, PR/review | Known revision, launch and inherited-flow checks |
| React API contract | Method/path, parameters/body, status, JSON envelope | OpenAPI and response examples; `{data}`, arrays and `{config}` differ |
| Quiz model and privacy | Question/choice IDs, server-only correct answer, active/required, threshold | Learner response has no answer key |
| Attempts and progression | Backend scoring, saved attempts, mandatory pass vs optional failure | Controlled passing/failing cases and unlock results; happy-path run alone is insufficient |
| Feedback | Identity, role, course ownership, recipient | Allowed and refused requests with existing linked records; source asks admin global intervention |
| Email | Business event, dynamic template, log/sandbox/provider | Five source-required situations, explained below |
| Settings | Database configuration vs environment secrets, protected CRUD | Admin lifecycle, thresholds, frequencies, trainer subscriptions and owned-course preferences |
| Jobs | Business handler vs HTTP/manual trigger vs scheduler, history, duplicate execution | Manual results, saved execution and separately observed scheduled run |
| Statistics | Audience, ownership filter, source data, averages/counts, cached snapshot | Known fixture arithmetic, refresh time and empty-state handling |
| Testing | Arrange/Act/Assert, negative tests, isolation, assertions vs requests | Postman/Newman and targeted automated tests, failures/skips recorded |
| Uploads | Multipart `file`, allowed content, size and role checks | Success 201; unsupported/missing 400; over 5 MiB 413 |
| Delivery | Docker services/ports, seed impact, secrets, reviewed Git history | Reproducible README, demo replay, teammate import, PR/review and contribution record |

## 📧 Correction: the five mandatory emails

Section 4 explicitly requires:

1. User registration.
2. Course enrollment.
3. **Forgotten password with a token or simulated link.**
4. Inactive learner reminder.
5. Trainer summary with simple statistics.

Earlier chat/LMS verification notes mistakenly named quiz completion as the fifth required situation. **That was incorrect.** Quiz-completion mail is not one of these five source requirements. Four real log events were observed (`user_registered`, `course_enrolled`, `inactive_learner_reminder`, `trainer_summary`). Current mounted auth routes are register/login/me; no forgot/reset endpoint is mounted in the inspected revision. The missing required journey is forgotten password. This is a source-inspected gap, not an endpoint test failure. SMTP receipt and cron timing are also unverified.

## 🧪 Evidence is not one single checkbox

- Prepared collection: 93 requests, covering the 54 documented operations in its reference.
- Agent isolated run: **90 executions / 209 assertions / 0 failures / 0 skips**, source `527ca48`, temporary API 3001 and MongoDB 27019; temporary setup removed.
- Learner's Docker run: initially refused connections; later supplied startup logs show MongoDB connected/API listening on 3000. Successful learner Newman replay is still pending.
- Second-developer replay, browser/CORS integration, SMTP delivery, scheduled timing, final review/merge and mastery remain separate checks.
- Postman evidence does not replace the targeted Jest/Supertest suite. No full Jest suite was rerun for this note update.

## 🎯 One next checkpoint

Run [public smoke](postman-newman-terminal.md) against the learner's Docker API. Complete when the terminal shows four requests, eleven assertions, zero failures and no skips. Then check one role login/profile. Keep the forgotten-password delivery gap visible to the squad.
