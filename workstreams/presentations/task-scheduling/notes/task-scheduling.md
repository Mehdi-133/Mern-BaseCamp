# ⏰ Task scheduling — quick review

🟡 **In progress** — discussed and documented; learner explanation pending.

## 🧠 Big idea

> A scheduler is an alarm clock that starts work: **WHEN → SCHEDULER → TASK → PROOF**.

- Trigger = when; task = what; frequency = how often.
- Once, recurring, or event-based are three trigger families.
- Cron is a Linux scheduling service; crontab contains its schedule entries.
- `0 2 * * * backup.sh` illustrates a daily 02:00 launch in the scheduler's timezone.
- Account, paths, permissions, environment, and timezone affect execution.
- Check exit code, logs, output, and missing-run alerts.

## ⚠️ Common trap

“The job was scheduled, so the backup worked.” Scheduling proves neither execution nor a usable backup. Repeated jobs can overlap; retries should avoid duplicate effects.

## 📖 Eloquent JavaScript foundation

- Chapter 11, printed pp. 185–186: asynchronous work and waiting.
- Chapter 20, printed pp. 361–362: Node scripts, command-line execution, and exit status.
- These pages were consulted locally. Cron and Windows Task Scheduler are outside these book lessons.

## 🧩 MERN connection

A scheduler could start a Node job that reads MongoDB and sends due LMS reminders. This is an example, not an implemented or verified feature.

## 🌐 Web culture

Developers keep logs and run history because background failures are easy to miss. A reliable job needs a clear policy for missed starts, overlapping runs, and retries.

## ✅ Remember

**Automatically started does not mean successfully completed.**

[Visual guide](../README.md) · [Understanding check](../exercises/README.md)
