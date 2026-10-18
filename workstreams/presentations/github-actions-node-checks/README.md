# ⚙️ GitHub Actions for Node.js Checks

> **Activity:** Veille — `GitHub Actions : automatiser les checks d'un projet Node.js`
>
> **YouCode ID:** `#82372`

## ⏰ Assignment status

🔁 **Review needed.** The authenticated YouCode intranet listed this activity under **To do (1)** on 2026-10-16. On 2026-10-17, a refreshed board showed **To do (0)**, **Doing (0)**, and **Done (0)**. No learner preparation, presentation delivery, cancellation, or completion is verified in this repository.

| Detail | Confirmed information |
| --- | --- |
| Date and time | Friday, 2026-10-16 at 09:30 |
| Duration | Not specified |
| Work mode | Listed as `en binôme` |
| Coworkers | Mohamed Bouthhandoust and Mouncif Benhar |
| Assigned by | Mehdi LARAIBI |
| Intranet state | To do on 2026-10-16; not visible on 2026-10-17 |

## 🎯 Purpose

Explain what GitHub Actions can automate, then focus on a Node.js team's current need: automatically run quality checks when code is pushed or proposed in a pull request.

The required focus is **continuous integration**, not a full Brief 2 deployment:

```text
push or pull request
        ↓
GitHub Actions workflow
        ↓
job on a runner
        ↓
checkout → setup Node.js → npm ci → npm test
        ↓
visible green or red result on GitHub
```

## 🧭 Required coverage

- GitHub Actions and the difference between a workflow, job, step, and action.
- Triggers such as `push`, `pull_request`, tags, manual runs, and schedules.
- Automation examples: lint, tests, build, audit, artifacts, documentation, notifications, and future deployment.
- CI compared with CD and why pull requests should run tests automatically.
- The roles of `actions/checkout`, `actions/setup-node`, and `npm ci`.
- Secrets that must remain protected.
- Why a simple workflow with reliable tests is better than unnecessary complexity.
- A minimal `.github/workflows/ci.yml` example explained line by line.

## 🗂️ Workspace

| Area | Purpose | Status |
| --- | --- | --- |
| [Concepts](./concepts/) | Concept lessons and future visual packs | ⬜ Not started |
| [Notes](./notes/) | Confirmed requirements and future speaking notes | 🟡 Assignment captured |
| [Exercises](./exercises/) | Learner-owned readiness checks | ⬜ No attempt saved |

## 🎯 Current mission

Spend **5 minutes** asking one teammate or the coach whether this veille was delivered or cancelled.

**Observable check:** a direct answer confirms the activity outcome and can be recorded without guessing from the board.

## ⚠️ Evidence boundary

- The intranet provides no duration and no separate submission deadline.
- No resource attachment was provided.
- The activity's disappearance from all three board columns is not completion evidence.
- The activity is not complete merely because its requirements are stored here.
- Do not change its intranet state until the learner starts or completes it personally.
