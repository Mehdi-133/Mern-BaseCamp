# 🧪 Brief 3 Exercise Roadmap

Each checkpoint should take about **5–15 minutes**. Answer in your own words before opening implementation code.

## 1. Stable baseline and non-regression

Create three rows: one behavior you believe works, one possible regression, and one unknown. For each row, write the exact request or command that would verify it.

**Complete when:** every row has an expected observable result and no row is marked “working” without evidence.

**Status:** 🟡 Current mission

## 2. API contract for React

Sketch the JSON shape for one `200`, one `400`, and one `403` response. Name the fields React can rely on.

**Complete when:** the three responses use one consistent success/error convention.

**Status:** ⬜ Not started

## 3. Quiz domain and safe projection

Classify `question`, `choices`, `correctAnswer`, `minimumScore`, and `required` as learner-visible, trainer-visible, or server-only.

**Complete when:** `correctAnswer` is excluded from every learner quiz payload.

**Status:** ⬜ Not started

## 4. Backend scoring

For a three-question quiz, compare submitted choices with an answer key and calculate the score. Then list which values the server may trust.

**Complete when:** the score is derived only from server-owned answers and learner selections.

**Status:** ⬜ Not started

## 5. Required versus optional progression

Predict whether the next module unlocks for: required-pass, required-fail, and optional-fail.

**Complete when:** all three decisions include one-sentence reasons.

**Status:** ⬜ Not started

## 6. Feedback permissions

Mark three requests allow/deny: trainer on own course, trainer on another course, learner reading another learner's feedback.

**Complete when:** each answer mentions role, ownership, or target identity.

**Status:** ⬜ Not started

## 7. Email boundary

For the inactive-learner reminder, name the event, template data, delivery driver, and one value that must stay secret.

**Complete when:** the provider can switch to `log` without changing the event rule.

**Status:** ⬜ Not started

## 8. Settings versus secrets

Place `emailsEnabled`, `summaryFrequency`, `inactiveDays`, `smtpHost`, `smtpPassword`, and `trainerCourseIds` in application data or environment configuration.

**Complete when:** secrets are never returned by CRUD endpoints or stored in Git.

**Status:** ⬜ Not started

## 9. Repeat-safe job

Write one sentence explaining how the same inactive-reminder job can run twice without sending the same reminder twice.

**Complete when:** the answer identifies a stable deduplication key or recorded run/event.

**Status:** ⬜ Not started; refine after importing the missing PDF

## 10. React-ready statistic

Define one statistic with: audience, source records, ownership filter, calculation, and example JSON result.

**Complete when:** React can render it without recalculating private backend rules.

**Status:** ⬜ Not started

## 11. Behavioral test

For “learner cannot see correct answers,” write one Arrange, Act, Assert outline and name the external dependency that should be faked if any.

**Complete when:** the assertion checks the response body, not only the status code.

**Status:** ⬜ Not started

## 12. Fresh-clone delivery

Read the eventual README as a new teammate and list the minimum commands from clone to one successful API request.

**Complete when:** environment, Docker, seed, docs, and verification request are all discoverable.

**Status:** ⬜ Not started

## 13. Terminal replay checkpoint — 30 October

1. Explain what `docker compose logs --tail 50 api` reads and why it cannot start a stopped engine.
2. Predict why a missing-token 401 can pass while a connection refusal fails.
3. Run the [four-request Newman smoke](../notes/postman-newman-terminal.md) and record its sanitized totals.

**Complete when:** the learner explains both distinctions and supplies four requests, eleven assertions, zero failures and no skips against the Docker API.

**Status:** 🟡 Commands discussed; startup logs supplied; successful smoke and independent explanation pending.
