# 🧪 Requests, assertions and expected refusals

> 🟡 **In progress — 30 October 2026.** Explained with project evidence; learner prediction check pending.
>
> 🧠 **Big idea:** a request calls the API; an assertion checks whether the response matches an expectation.

## 🔑 Key points

- One request can have several assertions: expected status, valid JSON and required fields.
- **200/201:** successful read/create. **204:** successful response without a body. **400:** invalid request. **401:** missing/invalid authentication. **403:** forbidden action. **409:** state conflict. **413:** oversized upload. The route contract supplies the exact expected response.
- An expected 401/403 is a successful negative test. A random error is not a pass: 404 for a nonexistent fixture does not prove 403 ownership protection.
- Authentication asks who the caller is; authorization asks whether this caller may perform this action on this record. A trainer role alone does not prove ownership; admin is not a universal bypass in the current API.
- Verify response content as well as status: learner quiz responses must not expose `correctChoiceId`.
- No HTTP response (`ECONNREFUSED`) explains later JSON parsing errors: diagnose the missing connection first.
- Zero failures with skipped requests is not full coverage. Ninety executions can repeat endpoints; 209 assertions are not 209 user journeys.

Tiny Postman example, supplied for revision rather than a completed learner exercise:

```javascript
pm.test("Anonymous profile is refused", () => {
  pm.response.to.have.status(401);
});
```

## 📖 Eloquent JavaScript foundation

- **Chapter 8, Bugs and Errors, printed pp. 135–136:** named tests check expectations; debugging traces the cause of observed failures.
- **Chapter 18, HTTP and Forms, printed pp. 317–318:** response status and body are separate parts of the protocol.
- **Boundary:** `pm.test` and `pm.response` belong to Postman, not standard JavaScript or the book.

## 🧩 MERN connection

Express middleware establishes identity, validates data and enforces permissions; controllers return observable results. Tests also inspect JSON objects and arrays consumed by React. Passing HTTP checks alone does not prove the browser integration.

## ⚠️ Common trap

Changing the expected status to whatever the server returns hides bugs. First verify the contract and arrange a valid fixture. Used resources/courses legitimately return 409 on deletion; unused records test successful deletion.

## 🌐 Web culture

Use Arrange → Act → Assert: prepare identities/data, send a request, then check the intended behavior. Tests demonstrate the tested cases, not mastery or every requirement.

## 🧪 Five-minute check

Predict whether these pass: expected 401/actual 401; expected 403/actual 404; expected 200/connection refused. Explain why. **Status: not attempted.**

## 🔗 Related learning

- [Newman terminal commands](postman-newman-terminal.md)
- [Fixture prerequisites](api-environments-and-fixtures.md)

> ✅ **Remember:** a correct refusal is a successful behavior check.
