# 🔗 API environments, tokens and linked fixtures

> 🟡 **In progress — 30 October 2026.** Project rules recorded; independent learner setup pending.
>
> 🧠 **Big idea:** an environment stores values; a fixture is prepared data that makes a scenario meaningful.

## 🔑 Key points

- `{{baseUrl}}`, role tokens and IDs are variables. This package keeps their values in the environment to avoid competing collection/global values.
- Each successful role login captures its own token and user ID. Failed login clears the old role identity first.
- Keep learner, trainer, admin and distinct other-user tokens separate. An invalid token tests 401, not another person's ownership.
- Linked IDs form a chain: trainer owns course → module belongs to course → resource and quiz belong to module → learner is enrolled → feedback belongs to that learner/course/module.
- Folder `05` creates a course, published module, link resource and optional quiz, publishes the course and enrolls the learner. It selects new IDs only after enrollment succeeds.
- `createdCourseId` and friends separate newly created data from existing fixtures. Re-running setup creates more records.
- `allowWrites=false` is the exported default. Set it deliberately to `true` only for approved disposable work; restore it afterward. Some GET routes save progress or create preferences and are guarded too.
- Database settings and role passwords are not interchangeable. `JWT_SECRET` signs backend tokens; it is never an API request credential.
- `SEED_DEMO_PASSWORD` configures the seed; setting it does not create users. Running the seed can reset passwords and replace matching course data.
- Config POST expects no existing singleton; enrollment/email code can create defaults. A lifecycle must establish state before expecting 201. This does not authorize deleting config from the working database.

## 📖 Eloquent JavaScript foundation

- **Chapter 8, printed pp. 135–136:** repeatable checks depend on controlled inputs and expectations.
- **Chapter 18, printed pp. 317–318:** a request addresses a specific server resource and receives a status/body.
- **Boundary:** MongoDB ObjectIds, JWT and Postman environments are project tools outside these book sections. Objects/arrays are the Chapter 4 foundation; this note does not advance Chapter 4 mastery.

## 🧩 MERN connection

MongoDB stores the relationships; Express and Node.js enforce the rules; React later uses returned IDs and its session token. Public exports must contain no usable passwords or JWTs. Marking a Postman field secret does not guarantee a safe export.

## ⚠️ Common trap

A well-formed 24-character ID can still identify the wrong module or a nonexistent record. Never invent IDs or reset the working database just to make a scenario pass.

## 🌐 Web culture

Use disposable data for destructive tests. Log-mode emails demonstrate generated events, not mailbox delivery. Preserve production/development data and separate automated test evidence from the intended deployment.

## 🧪 Five-minute check

Draw the fixture chain in one line and explain why an unrelated module cannot prove a valid course journey. **Status: not attempted.**

## 🔗 Related learning

- [Assertions and negative tests](api-assertions-and-negative-tests.md)
- [Brief 3 delivery checklist](brief-3-delivery-revision.md)

> ✅ **Remember:** valid identity + related records + known state → meaningful API evidence.
