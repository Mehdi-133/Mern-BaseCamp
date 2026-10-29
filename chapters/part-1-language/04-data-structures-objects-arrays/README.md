# Chapter 4 - Data Structures: Objects and Arrays

## 🎯 Status

> 🧭 **28 October workshop preparation:** [AI with Context](../../../workstreams/presentations/six-file-context-engineering/README.md) researches the supplied JavaScript Mastery six-file method, with visual maps and a two-person workshop plan. Demo execution and understanding remain pending; Chapter 4 status is unchanged.

> 🤝 **28 October continuity:** [AI DEV SQUAD](../../../docs/ai-dev-squad/README.md) collaboration kit prepared and four read-only LMS reviews completed. This is tooling/documentation evidence; no Chapter 4 exercise, book concept or understanding status changed.

> 🎤 **26 October presentation preparation:** [visual scheduled-task workflow](../../../workstreams/live-coding/mern-scheduled-tasks/workflow.md) prepared with a session map, architecture comparison and proof flow before live coding. No Chapter 4 completion change.

> ⏰ **26 October continuity:** scheduled-task [manual-trigger checkpoint](../../../workstreams/live-coding/mern-scheduled-tasks/notes/manual-trigger.md) discussed; diagnostic answer correct. No Chapter 4 progress changed.

> 🧪 **22 October continuity:** learner selected the [Brief 2 Jest/Supertest checkpoint](../../../workstreams/sprints/sprint-2/briefs/brief-2/notes/jest-and-supertest.md). Explanation prepared; answers pending. No Chapter 4 exercise or status changed.

> 🧭 **14 October continuity:** [Brief 2 and student-life recap](../../../sessions/history/2026-10-14-brief-and-student-life.md) saved. No new Chapter 4 exercise or understanding check was completed; existing chapter statuses remain open.

🟡 **In progress** — core concept study is ready; slide creation, final synthesis, quiz, and rehearsal remain.

> 🎤 Activity workspace: [JavaScript Data Structures Presentation](../../../workstreams/presentations/javascript-data-structures/)

## 🎤 Presentation checkpoint

- ✅ Studied `Array`, `Object`, `Map`, and `Set` through MERN examples.
- ✅ Practised choosing structures for ordered lists, lookup by ID, and unique values.
- ✅ Compared traversal, transformation, search, filtering, sorting, and grouping.
- ✅ Connected source data, derived structures, object identity, and JSON boundaries.
- 🔁 Added `structuredClone()` as a modern nested-copy option; the prediction and explanation check is still pending.
- 🟡 Build the final comparison and two mini-cases into the Canva deck.
- ⬜ Create the final quiz and rehearse the oral explanation.

## Source

- Printed pages: 58-83
- Main topics: arrays, objects, properties, methods, mutability, array loops, destructuring, JSON, and linked lists

## Learning goals

- Choose between an array and an object for a simple problem.
- Add, remove, access, and iterate over array elements.
- Represent one real-world item with an object.
- Build a collection as an array of objects.
- Explain stacks, queues, and linked lists in simple words.

## Work areas

- `exercises/` - learner solutions for the class presentation preparation.
- `examples/` - add only when a book example is studied.
- `experiments/` - add only when a variation is needed to test an idea.

## Completion checklist

- [ ] Read the chapter attentively.
- [ ] Type, predict, and run important examples.
- [ ] Complete the array basics exercise.
- [ ] Complete an object and array-of-objects exercise.
- [ ] Explain stacks and queues in simple words.
- [ ] Attempt the linked-list exercise before viewing a solution.
- [ ] Prepare and rehearse the class presentation.
- [ ] Record questions and vocabulary.
- [ ] Run relevant checks.
- [ ] Update progress and the current handoff.

## Discoveries

- A data structure organizes values according to how a program needs to use them.
- With `reduce()`, the accumulator must start with the correct type and each iteration must return the updated accumulated value.
- An array is useful for an ordered collection; a `Map` is useful when a known key should retrieve one related value.
- `Map.get()` returns a value or `undefined`, while `Map.has()` safely checks whether a key exists—even when its value is `0`.
- `Map` keys preserve type and object identity, so `1`, `"1"`, and `{ id: 1 }` are different keys.
- A `Set` removes repeated primitive values while preserving the order of their first appearance.
- Separate objects remain separate `Set` values unless they share the exact same reference.
- `find()` returns the first match or `undefined`, while `filter()` always returns a new array of all matches.
- Default `sort()` compares values like text and mutates its array; copy first and provide a comparator when needed.
- `forEach()` performs an action for every item, while `map()` transforms every item into a new array.
- Grouping keeps all items but organizes them under shared keys.
- One source array can produce a `Set` for uniqueness and a `Map` for lookup, but those derived containers do not update automatically.
- `Map` and `Set` should be converted to an object or array before crossing a JSON API boundary.

## 🔁 Questions to review

- When does `structuredClone()` create independent nested data?
- Why are spread syntax and `Object.assign({}, original)` still shallow copies?
- Which kinds of values should not be passed blindly to `structuredClone()`?

## Challenge statistics

| Challenge | Status | Score |
| --- | --- | ---: |
| Study session queue | Not started | - |
| Student results report | Not started | - |
| Car statistics API | Review needed | 5/10 |

- Attempted: 1 of 3
- Complete: 0 of 3
- Completion rate: 0%

## Exercises

| Exercise | Status | File | What I learned |
| --- | --- | --- | --- |
| Array basics | Not started | `exercises/01-array-basics.js` | To complete after the exercise |
| Study session queue | Not started | `exercises/02-study-session-queue.js` | To complete after the challenge |
| Student results report | Not started | `exercises/03-student-results-report.js` | To complete after the challenge |
| Car statistics API | Review needed | `exercises/04-car-stats-api.js` | The server runs, but calculation, route, and response issues remain |

## Verification

All four starter files pass JavaScript syntax checks.

The completed `Map`, `Set`, data-operations, and derived-structures concept notes were checked for clean Markdown, accurate examples, Web culture connections, and presentation-ready takeaways.

The latest Challenge 04 attempt was reviewed:

- Correct: total cars, total price, and the dataset's average value.
- Needs correction: city counts, most expensive car, missing cheapest car, average rounding, route path, and plain-text response.
- Added: an Express server entry point, an EJS result page, and an npm start script for the challenge.
- Passed: `node --check` for both JavaScript files.
- Runtime: Express and EJS are installed, and the result page renders successfully at `/cars/statistics`.
- Live route check: `/cars/statistics` returns HTTP 200, while the required `/cars/stats` returns HTTP 404.
- Checkpoint: the learner attempt was preserved in local commit `1edbdfe` without marking the exercise complete.
- Runtime checkpoint: dependencies and the port change were preserved in local commit `5620e29`.

### Challenge 04 evaluation - 5/10

| Requirement | Point | Result |
| --- | ---: | --- |
| Preserve and use the 12-car dataset | 1 | Passed |
| Calculate total cars | 1 | Passed: `12` |
| Calculate total price and average | 1 | Passed: `1909992` and `159166` |
| Count cars by city | 0 | Failed: every city is one too high |
| Find the most expensive car | 0 | Failed: returns Dacia Logan instead of Toyota C-HR |
| Find the cheapest car | 0 | Missing |
| Implement `GET /cars/stats` | 0 | Failed: current path is `/cars/statistics` |
| Return the required plain-text output | 0 | Failed: renders an EJS page instead |
| Organize the solution into readable methods | 1 | Passed |
| Start and run the endpoint | 1 | Passed: the EJS page returns HTTP 200 |

The next review will replace this score only after rerunning the full requirement checklist.

## 🧩 Brief 2 foundation link — 2026-10-12

The [roles and ownership lesson](../../../workstreams/sprints/sprint-2/briefs/brief-2/concepts/roles-and-resource-ownership/) applies object properties and array `includes()` to `req.user.role`. Understanding remains pending; this adds no completed chapter exercise.

The [controlled file upload lesson](../../../workstreams/sprints/sprint-2/briefs/brief-2/concepts/controlled-file-uploads/) shows how one uploaded file becomes structured MongoDB metadata: module reference, type, stored path, original name, size, and order. This is a practical object-modeling connection; its understanding and runtime checks are still pending and do not complete a Chapter 4 exercise.

## 🧩 Brief 3 foundation link — 2026-10-19

The [Brief 3 concept roadmap](../../../workstreams/sprints/sprint-2/briefs/brief-3/concepts/) reuses Chapter 4 objects and arrays for nested quiz questions, answer choices, attempts, and safe response shapes. This is an application link only; no Chapter 4 exercise or Brief 3 understanding check was completed by creating the roadmap.
