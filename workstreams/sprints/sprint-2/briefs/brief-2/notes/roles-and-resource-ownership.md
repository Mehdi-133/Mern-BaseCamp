# 🛡️ Roles and resource ownership — quick review

> 🟡 **In progress** — prepared from the learner's requested topic and current code; understanding check pending.

> 🧠 **Big idea:** a valid login does not grant every permission.

## 🔑 What we are reviewing

- Authentication: verify identity and create `req.user`.
- Authorization: check whether that role may perform the requested action.
- Ownership: check whether this course belongs to this trainer.
- `authorize(...allowedRole)` returns middleware; `includes()` checks role membership.
- `401`: authentication required/invalid. `403`: authenticated but forbidden. `404`: target missing.
- Existing role middleware passed four isolated checks. HTTP integration and ownership are not verified.

## 📚 What you should be able to explain

- Why authentication must run before authorization.
- Why trainer A cannot manage trainer B's course.
- Why public registration must not accept privileged roles.
- How `next()` differs from `return next(error)`.
- How child modules/resources inherit the course ownership boundary.

## 📖 Eloquent JavaScript foundation

- **Chapter 3, Functions, printed pp. 54–56:** separate responsibilities into named functions; functions can return functions.
- **Chapter 4, Data Structures: Objects and Arrays, printed pp. 61–62 and 69:** object properties hold data; `includes()` checks array membership.
- **Chapter 18, HTTP and Forms, printed pp. 318–319:** requests identify an action and resource; responses communicate status.
- Consulted the local PDF. Express authorization, JWT policy, and Mongoose ownership are practical applications, not tools taught directly by these pages.

## 🧩 MERN connection

MongoDB stores identity and ownership; Express middleware checks permissions on Node.js. React can reflect those decisions but cannot replace backend checks.

## ⚠️ Common trap

Do not treat a role check as an ownership check. On 14 October, fresh source inspection found a `trainer` reference in the Course schema. A stored owner reference still needs to be checked by each relevant endpoint.

## 🔎 14 October resource-route review

- Resource GET is currently public. Its query filters by module and sorts by order; neither operation proves permission or unlock status.
- Resource POST/PUT contain authentication and trainer-role middleware, but validation currently runs first. Review authentication → authorization → input validation → controller.
- Resource DELETE has a trainer-role gate; its documentation explicitly excludes course-ownership checks.
- The [daily checkpoint](./2026-10-14-brief-checkpoint.md) contains an explained target workflow. This was a source review only; allowed/denied HTTP requests and learner understanding are still pending.

Book foundation revisited in the local PDF: Chapter 4, printed p. 61 (object properties/methods), and Chapter 18, printed p. 318 (request method, resource path, and server responses). Express permission rules are the project's practical application, not a library taught on those pages.

## 🌐 Web culture

Use explicit role/action rules, scoped resource access, and allowed/refused API tests. Role changes after JWT issuance require a deliberate current-account policy.

## 🔗 Related learning

- [Lesson, workflow, pictures, and code explanation](../concepts/roles-and-resource-ownership/)
- [JWT quick note](./jwt-authentication.md)
- [Three-request exercise](../exercises/roles-and-resource-ownership.md)

> ✅ **Remember:** role permits the action; ownership limits its target.
