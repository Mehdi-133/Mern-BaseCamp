# ▶️ Videos for the scheduled-task live coding

> 🟡 **Selected, not watched or completed.** Links and chapters were found in YouTube-indexed descriptions on 26 October 2026. Full videos were not reviewed; fetching watch pages directly failed.

## 1. Start with Node.js scheduling

[Scheduling Tasks in Node.js | Cron Jobs in Real Projects — Dipesh Malvia](https://www.youtube.com/watch?v=6gmdFPlkuhQ)

- Watch **00:58–05:59** first: node-cron package, simple scheduled task, cron expression.
- Continue through **15:38** to see the record-archival example. Treat that as an example to understand, not a task to copy into the LMS.
- Connection: `statsRefresh` is our business function; scheduling calls it at the configured time.
- Pause check: explain WHAT the function does and WHEN the scheduler calls it.

## 2. Understand our containers

[Setup Node.js Microservice & MongoDB Using Docker Compose | Setup Full Stack in Minutes — codeonedigest](https://www.youtube.com/watch?v=ednRWe8gkA8)

- Watch **04:54–13:15**: Compose file, then building and starting Node.js/MongoDB services.
- Connection: our practice API and MongoDB run as separate services.
- Pause check: explain why the API can stop while MongoDB stays running, and why the job still needs MongoDB.

## 3. Optional second explanation

[Schedule Tasks in Node.js with Cron Jobs | node-cron Tutorial Step by Step — vrfEducationEnglish](https://www.youtube.com/watch?v=lDp3t8EZ50Q)

- The description covers scheduled tasks, cron expressions, and distinctions between scheduling tools.
- Use this if the first explanation feels too fast; do not add more libraries to our demo just because they appear in a video.
- Pause check: explain why a start log does not prove that the expected count was produced.

## 🎯 How to use this watchlist

Spend roughly **25–35 minutes**, including pauses, on the targeted sections of videos 1 and 2. Then return to our [workflow](../workflow.md) and implement the small published-course count. This is a suggested study budget, not a measured viewing duration.

Videos supplement our repository lesson; current library behavior and project code remain the technical reference. No video proves our demo works.
