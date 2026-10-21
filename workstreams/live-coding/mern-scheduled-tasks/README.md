# ⏰ Scheduled Tasks in a Dockerized MERN Application

> 🟡 **Preparing** — YouCode live coding `#82875` is scheduled for **Monday, 26 October 2026 at 14:30**. The activity is confirmed; Mehdi's preparation, rehearsal, and live execution are not yet verified.

## 📅 Confirmed activity record

| Detail | Confirmed information |
| --- | --- |
| Activity | Live Coding — *Tâches planifiées dans une application MERN avec Docker : explorer les architectures possibles* |
| YouCode ID | `#82875` |
| Date and time | Monday, 26 October 2026 at 14:30 |
| Duration | Not specified |
| Work rule | Individual |
| Learner | Mehdi Karbitou |
| Assigned by | Mehdi LARAIBI |
| Board state on 21 October | `To do` |
| Attached resources | None |

## 🎯 Purpose

After learning scheduling at the operating-system level, this session moves the idea into a containerized MERN application. The goal is to compare possible scheduler locations and make **one representative Brief 3 job** work in a controlled demonstration.

## 🧭 Points to cover

1. Separate the business function from the mechanism that triggers it.
2. Keep a manual way to run and verify the business function.
3. Compare three locations: inside the API process, in a dedicated process, or through an external/host scheduler that calls the container.
4. Make frequency, timezone, configuration, and start/success/failure logs explicit.
5. Discuss shutdown, restart, multiple instances, overlapping runs, and duplicate work.
6. Choose a proportionate solution and verify its behavior.

## 🧪 Demonstration boundary

- A small indicator refresh using a few records is enough.
- The trainer compares architectures; the demonstration implements only one prepared path.
- A separate worker is **not required**.
- This activity does **not** provide a full solution for all three Brief 3 jobs.
- Expected evidence: a demonstrable business function, a reproducible trigger, and readable traces.

## 🗂️ Learning route

| Area | Purpose | Status |
| --- | --- | --- |
| [Concepts](./concepts/) | Reuse the verified scheduling foundations and connect them to Docker/MERN | 🟡 References ready |
| [Notes](./notes/) | Preserve assignment facts and evidence boundaries | ✅ Recorded |
| [Exercise](./exercises/) | Prepare one architecture-and-proof plan | ⬜ Not started |
| [Reviews](./reviews/) | Record rehearsal, runtime checks, and feedback later | ⬜ No attempt saved |

## 🔗 Brief connection

This live coding prepares [Brief 3 concept 9: scheduled jobs, idempotency, and run history](../../sprints/sprint-2/briefs/brief-3/concepts/README.md). It complements the existing [task-scheduling presentation lesson](../../presentations/task-scheduling/) instead of duplicating it.

## 🚀 Current mission

Complete the [15-minute architecture-and-proof plan](./exercises/).

**Ready check:** the plan names one business function, one manual trigger, one scheduler location, three useful log outcomes, and one Docker risk to verify.
