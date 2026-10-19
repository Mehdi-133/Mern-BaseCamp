# Learning Progress

## ⏰ Task scheduling presentation — 2026-10-19

- 🟡 Prepared a [simple visual guide](workstreams/presentations/task-scheduling/) for the learner-reported presentation tomorrow, 20 October.
- Read all eight shared slides and speaker notes; saved the slide story, French/English vocabulary, cron decoder, overlap chart, quick note, and three-question check.
- Preparation is saved; learner understanding, rehearsal, scheduler execution, and delivery are unverified. No chapter completion changed.
- **Next:** explain the nightly-backup trigger, scheduler, task, and proof in 30 seconds.

## 🚀 Sprint 2 — Brief 3 intake — 2026-10-19

> 🟡 **In progress:** the final LMS API brief is saved and analyzed under [`workstreams/sprints/sprint-2/briefs/brief-3/`](workstreams/sprints/sprint-2/briefs/brief-3/). This records the mission and learning route; it does not certify any new application behavior.

Milestone recap: [19 October 2026 — Sprint 2 Brief 3 intake](sessions/history/2026-10-19-brief-3-intake.md).

| Brief 3 area | Current evidence | Status |
| --- | --- | --- |
| Schedule | 19–30 October 2026 | ✅ Confirmed |
| Work mode | Squad; individual contributions must stay visible | ✅ Confirmed; members not named in supplied text |
| Source intake | Official page, learner-supplied text, requirements, deliverables, and criteria saved | ✅ Complete for supplied text |
| Missing continuation | Section 6 points to `brief-03-sprint-02-version-simplonline.pdf` | 🔁 PDF still needed |
| Existing LMS baseline | Auth, roles, uploads, progress, trainer reporting, tests, Swagger, seed, and Docker artifacts found in source | 🟡 Runtime and shared-branch verification pending |
| New product scope | Quiz, attempts, scoring, feedback, email, configuration, jobs, stats, and React contract | ⬜ Not verified |
| Concept path | Twelve dependency-ordered concepts with short checks | ✅ Roadmap prepared; understanding checks not started |
| Delivery visual | Five-stage dependency route with cross-cutting safety rules | ✅ Saved; final visual verification recorded in its tracker |

### 🎯 Current mission

Complete the [baseline and regression micro-task](workstreams/sprints/sprint-2/briefs/brief-3/exercises/#1-stable-baseline-and-non-regression): record one believed-working behavior, one possible regression, and one unknown with the exact observable check for each.

**Completion check:** no item is called working without a reproducible result.

## 📦 Brief 2 Multer upload checkpoint — 2026-10-19

> 🟡 **In progress:** a real resource-upload implementation exists and its basic version is merged. Runtime verification and Mehdi's concept explanation remain open.

| Upload evidence | Status |
| --- | --- |
| Multer dependency and `upload.single("file")` route | ✅ Present |
| PDF/JPEG/PNG filter, 5 MiB limit, UUID stored name | ✅ Merged through `3aeba27` |
| Module-linked MongoDB metadata and failure cleanup | ✅ Merged through `3aeba27` |
| Course ownership and file-signature comparison | 🟡 Present in `883aa0e` on `feature/FAL-46-upload-module-file`; not confirmed on `main` |
| Upload-focused automated tests | ⬜ Not found |
| Accepted and rejected HTTP upload cases | ⬜ Not rerun in this checkpoint |
| Concept lesson and verified workflow visual | ✅ [Saved under Brief 2](workstreams/sprints/sprint-2/briefs/brief-2/concepts/controlled-file-uploads/) |
| Learner understanding exercise | ⬜ [Prepared; answers pending](workstreams/sprints/sprint-2/briefs/brief-2/exercises/controlled-file-uploads.md) |

Related class references are recorded separately: [MERN file-upload presentation](workstreams/presentations/mern-file-upload/) and [secure resource-upload live coding](workstreams/live-coding/secure-resource-upload/). Their `Finished` board state is not claimed as Mehdi participation or delivery evidence.

## 🔁 YouCode activity visibility change — 2026-10-17

- The refreshed Class Activities board now shows **To do (0)**, **Doing (0)**, and **Done (0)**.
- The GitHub Actions veille `#82372`, previously listed under **To do** on 2026-10-16, is no longer visible in any column.
- 🔁 **Review needed:** disappearance from the board does not prove that the presentation was delivered, completed, or cancelled.
- 📂 The previously confirmed assignment requirements remain stored in [the presentation workspace](workstreams/presentations/github-actions-node-checks/README.md).
- ✅ **Current mission:** ask one teammate or the coach to confirm the activity outcome and record the answer.
- ⚠️ No new YouCode activity is visible, and no preparation or delivery evidence was added.

## 📊 Latest brief evidence — 2026-10-14

- 🟡 [Today's checkpoint](workstreams/sprints/sprint-2/briefs/brief-2/notes/2026-10-14-brief-checkpoint.md) collects the mentor's **55/100** snapshot at `cf906bd`, team-work reports, and a fresh resource-route source review.
- 🔁 Upload, trainer views, and tests are missing in that assessment; JWT, roles, and progression are partial. No API runtime or new learner mastery was verified in this recap.
- 🎯 Next mission agreed in today's chat: E08 resource-model inspection, planned for 22:00 Africa/Casablanca. Earlier roles/JWT/non-regression exercises stay open.
- 🎓 [Student-life recap](sessions/history/2026-10-14-brief-and-student-life.md): pair check-in evidence, evening plan, pending video, and unfinished cloud-notification setup.
- 📖 Chapter-level status is unchanged. Older checkpoints below are retained as historical evidence.

## Current position

- Current part: Part 1 - The JavaScript language
- Main direction: develop MERN JavaScript skills by connecting every practical concept to *Eloquent JavaScript*
- Current focus: Sprint 2 — Brief 3 intake and inherited Brief 2 baseline verification
- Chapter status: In progress; the class presentation was delivered on 2026-10-12
- Earlier chapters: Not completed; Chapter 1 remains not started
- Last meaningful update: 2026-10-19 - Documented Brief 2's Multer upload flow, merged-versus-branch evidence, and related class activities
- Next learning target: explain how multipart data becomes `req.file` and a module-linked MongoDB resource
- Next repository target: complete the Brief 2 controlled-upload understanding check; Brief 3 baseline verification remains open

## 🤝 Sprint 2 — Brief 2 checkpoint

> 🟡 **In progress:** the full brief and its learning workspace are stored under [`workstreams/sprints/sprint-2/briefs/brief-2/`](workstreams/sprints/sprint-2/briefs/brief-2/).

| Brief area | Current status |
| --- | --- |
| Sprint and brief identity | ✅ Sprint 2 — Brief 2 |
| Team | ✅ Binôme with Maroua |
| Official Simplonline source | ✅ [Authentification, accès et progression LMS](https://maghreb.simplonline.co/classrooms/4867b8e5-eb61-4ad3-a538-a88b9ebb5957/briefs/89986592-a062-464e-bd28-b1e00fe16171) |
| Assignment | 🟡 Group assignment — To be submitted; workspace **Lake Titans** |
| Full brief intake | ✅ Requirements, deadline, assessment, deliverables, and risks recorded |
| Brief content and analysis | ✅ Original source, structured guide, learner-friendly analysis, and two reviewed diagrams saved |
| Concept and exercise roadmap | ✅ Twelve ordered concepts with one short understanding exercise each |
| Book-to-MERN concept notes | 🟡 Required note pattern saved; Zod, JWT, and Clerk examples updated |
| Existing API baseline | 🟡 Read-only code inventory complete; runtime smoke test pending |
| Confirmed technical task | 🟡 Secure the full LMS backend from authentication through sequential progress |
| JWT dependency and environment safety | ✅ Verified |
| JWT concept visual pack | ✅ Concept card, login flow, usage checklist, and image tracker verified |
| Clerk, Clerk SDK, CLI, and MCP | 🔁 Review needed: concept note and diagrams saved; learner explanation pending |
| `ghost ai` source review | ✅ Accessible project conversation inventoried and mapped to the saved Clerk lesson |
| Clerk project decision | ✅ Custom JWT required by the brief; Clerk remains comparison knowledge only |
| Login schema | 🟡 Saved attempt appears complete; behavior checks pending |
| Login controller, route, and token response | 🟡 Saved implementation exists; live verification pending |
| Authentication middleware and role authorization | 🔁 JWT middleware review needed: isolated valid, expired, and invalid-token checks passed; route integration and role authorization remain |
| Enrollment, upload, progress, and trainer endpoints | 🟡 Basic Multer upload merged; ownership/signature hardening branch-only; runtime tests pending; other flows remain incomplete |
| Tests, API docs, and reproducible runtime | 🟡 Partial Swagger and Docker setup; automated tests absent |
| Official title and source link | ✅ Verified on Simplonline on 2026-10-12 |
| Requirements and evaluation criteria | ✅ Recorded from the supplied brief text |
| Deliverables and deadline | ✅ Recorded; deadline 2026-10-16 |
| Responsibility split | ⬜ Not recorded yet |

The repository will be updated from confirmed briefing information and verified work only.

## 🎤 Data-structures presentation checkpoint

> ✅ **Delivered on 2026-10-12.** Mehdi reported that the presentation went well. This confirms delivery, while the unreviewed deck corrections, quiz, and remaining concept checks stay open.
>
> Workspace: [`workstreams/presentations/javascript-data-structures/`](workstreams/presentations/javascript-data-structures/)

| Presentation area | Status |
| --- | --- |
| Arrays, objects, references, mutation, and identity | ✅ Covered |
| `Map` for key-value lookup | ✅ Covered |
| `Set` for unique values | ✅ Covered |
| Traverse, transform, search, filter, sort, and group | ✅ Covered |
| Source data, derived structures, and JSON boundaries | ✅ Covered |
| Deep copying nested data with `structuredClone()` | 🔁 Review needed: prediction and explanation pending |
| Concept-owned pictures, diagrams, and explanations | ✅ Five visual packs complete: concept cards, exact diagrams, trackers, alt text, and explanations |
| Final `Array` vs `Object` vs `Map` vs `Set` comparison | 🟡 Complete inside the slides |
| Required mini-cases | 🟡 Turn the learned examples into audience questions |
| Slide design, final quiz, and oral rehearsal | 🟡 Slides 1–6 rehearsed for 31:44; presentation delivered; final deck corrections and quiz remain unverified |

> 🧭 **Honest status:** presentation delivery is confirmed by the learner. No mentor score or audience feedback was recorded, and the final PDF inspection, four code corrections, quiz, and `structuredClone()` understanding check remain unverified.

## 🧑‍🏫 Mentor checkpoint — Sprint 1, Brief 3

> 🎉 **Result:** Brief 3 validated on 2026-10-07.
>
> The full feedback is stored in [`workstreams/sprints/sprint-1/briefs/brief-3/feedback/mentor-evaluation.md`](workstreams/sprints/sprint-1/briefs/brief-3/feedback/mentor-evaluation.md).

### ✅ Validated strengths

- Strong technical foundation: MVC, OOP, Repository pattern, interfaces/contracts, and Sequelize.
- Functional Express/EJS understanding: routes, dynamic parameters, filtering, controllers, and views.
- Healthy planning habit: describe the controller, route, view, and dynamic route in comments before coding.
- Good separation of responsibilities with a controller class and `this.hotels = hotels`.
- The remaining Express/EJS issues are mainly syntax recall, not missing understanding.
- The *Eloquent JavaScript* repository shows responsible use of AI as a learning coach.

### 🎯 Improvement priorities

- Practise Express routes, EJS views, dynamic parameters, array filters, and raw SQL without generative AI.
- Use short exercises regularly to make JavaScript syntax more automatic.
- Keep writing meaningful parts of each deliverable personally, even when it takes longer.
- Explain technical choices more clearly during oral presentations.
- Strengthen raw SQL, especially `JOIN` and filtered queries without Sequelize.

### 🛠️ Priority action tracker

| Practice task | Completion evidence | Status |
| --- | --- | --- |
| 🏙️ `/hotels` filtered by city | Plan comments, controller, route, view, working result, and a 3-minute explanation | ⬜ Not started |
| ⭐ `/hotels` filtered by star count | Plan comments, controller, route, view, working result, and a 3-minute explanation | ⬜ Not started |
| 🛎️ `/hotels` filtered by `amenities` | Plan comments, controller, route, view, working result, and a 3-minute explanation | ⬜ Not started |
| 🗃️ One simple raw SQL `JOIN` | Handwritten query, verified result, and a clear explanation without Sequelize | ⬜ Not started |

### 🛡️ Learning rule

The first attempt is completed without generative AI: write the plan in comments, implement it, and explain the flow. AI may give a small hint or review the saved attempt afterward. A task becomes complete only when its behavior and explanation are both verified.

> 💡 **Remember:** AI is your coach and reviewer—not the person taking your practice attempt.

## Challenge statistics

| Statistic | Count |
| --- | ---: |
| Practice challenges prepared | 3 |
| Challenges attempted | 1 |
| Challenges complete | 0 |
| Challenges needing review | 1 |
| Challenges not started | 2 |

- Latest evaluation: Challenge 04 - **5/10** (`Review needed`)
- Completion rate: **0%** - an attempt is counted as complete only after all required behavior is verified.

## Today's plan - 2026-10-11

- [ ] Implement and verify the authenticated user-check route.
- [ ] Prepare tomorrow's JavaScript data-structures presentation.
- [ ] Meet Marwa at 18:00 to agree on the workshop goal, responsibilities, and next actions.
- [ ] Complete the route exercise assigned by the mentor.
- [ ] Complete one timed presentation rehearsal.

Complete the tasks in this order because the route is today's first implementation priority, while the final rehearsal depends on the presentation preparation.

The five tasks are verified as timed events in Mehdi's primary Google Calendar. Each event has a 10-minute popup reminder; the workshop meeting also has a 30-minute reminder. The active **Calendar task coach** checks the calendar every 30 minutes from 08:00 to 21:30 in `Africa/Casablanca` and stays quiet when nothing is actionable.

> ⚠️ **Evidence boundary:** the calendar and reminder setup is complete. The route implementation, meeting, mentor exercise, presentation corrections, and rehearsal remain unverified.

## Milestones

| Milestone | Status | Evidence |
| --- | --- | --- |
| Learning workspace and shared agent rules | Complete | Root documentation, chapter structure, and handoff files |
| Git repository initialized on `main` | Complete | Local `.git` repository |
| Notion learning tracker connected | Complete | Learning hub, 21-chapter tracker, and progress log inside Mehdi's Board |
| Daily plan connected to Google Calendar | Complete | Five verified timed events for 2026-10-11 with popup reminders |
| Recurring calendar task coach | Complete | Active 30-minute checks from 08:00 to 21:30 with actionable-only updates |
| Public GitHub navigation and clone guide | Complete | Root README with visitor paths, setup guidance, repository map, and status meanings |
| Chapter 4 class presentation follow-up | In progress | Presentation delivered; artifact checks, quiz, and one concept review remain |
| Part 1 - JavaScript language | Not started | Chapters 1-12 |
| Part 2 - Browser JavaScript | Not started | Chapters 13-19 |
| Part 3 - Node.js | Not started | Chapters 20-21 |

## Completed chapters

None yet.

## Review queue

Add topics here when they need spaced repetition or another explanation.

- Express/EJS syntax: `res.render`, EJS tags, routes, and dynamic parameters.
- Array filtering without assistance.
- Raw SQL `JOIN` and filter queries.
- Three-minute explanations of technical choices.
- Clerk tool boundaries: runtime SDK vs development CLI vs optional AI MCP support.
- JWT verification middleware: Bearer parsing, `jwt.verify()`, `decoded.sub`, `req.user`, `next()`, and response-ending `return` statements.

## 🛡️ Roles and ownership — 2026-10-12

🟡 Lesson, quick note, three visuals, and exercise prepared at the learner’s request. Existing `authorize` passed four direct checks (missing user, learner, trainer, admin). Full HTTP integration, ownership enforcement, and learner understanding remain unverified. No application code changed.
