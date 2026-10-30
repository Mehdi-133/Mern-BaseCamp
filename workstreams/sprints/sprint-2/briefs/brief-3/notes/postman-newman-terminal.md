# 📬 Run Postman requests with Newman

> 🟡 **In progress — 30 October 2026.** Command explained; successful learner Docker replay still pending.
>
> 🧠 **Big idea:** Newman runs saved Postman requests and their JavaScript checks in the terminal.

## 🔑 Public smoke command

From `C:/Users/LENOVO/Desktop/fondations_API_LMS`, with the API running:

```powershell
npx --yes newman run docs/postman/LMS-Frontend.postman_collection.json `
  -e docs/postman/Local-Docker.postman_environment.json `
  --folder "00 Public smoke" `
  --reporters cli `
  --timeout-request 10000
```

| Part | Meaning |
| --- | --- |
| `npx --yes newman` | Executes Newman; npm may download it if unavailable. `--yes` accepts npm's install prompt, not API-write permission |
| `run ...collection.json` | Imports and executes the saved collection |
| `-e ...environment.json` | Loads variables, including normal Docker `baseUrl=http://localhost:3000` |
| `--folder "00 Public smoke"` | Runs only that folder |
| `--reporters cli` | Prints the result in the terminal |
| `--timeout-request 10000` | Allows up to ten seconds per request |
| PowerShell backtick | Continues the command onto the next line; keep it as the final character, without trailing spaces |

Only this selected public folder reads without deliberately changing learning records. It sends four requests and expects eleven assertions:

| Request | Expected status | Reason |
| --- | ---: | --- |
| `GET /` | 200 | API responds |
| `GET /api/courses` | 200 | Published catalogue shape is valid |
| `GET /api/auth/me` without token | 401 | Anonymous user refused |
| `GET /api/auth/me` with invalid token | 401 | Invalid identity refused |

Expected runner result: **4 requests, 11 assertions, 0 failures**. After the command, `$LASTEXITCODE` should be `0`. A skipped request is untested.

## 🔑 Login is the next checkpoint

Folder `01 Role login` needs three existing demo accounts and their actual local passwords. On a disposable/local environment, set `learnerPassword`, `trainerPassword` and `adminPassword` privately. Select the login folder with the same command and `--folder "01 Role login"`. Expected: **3 requests, 9 assertions, 0 failures**. The exported environment intentionally has empty passwords and tokens; importing it does not create accounts. A 401 login can mean wrong credentials, missing account or suspended user; read the response before resetting anything.

Passwords passed using `--env-var` are visible in process arguments even if prompted securely first. Prefer a private ignored local environment file for CLI work, restrict its access, and never add it or exported JWTs to Git. Do not paste credentials into a shared terminal transcript.

## 📖 Eloquent JavaScript foundation

- **Chapter 8, printed pp. 135–136:** automated checks repeat known expectations and expose regressions.
- **Chapter 18, printed pp. 317–318:** HTTP methods, connection, response status and body.
- **Boundary:** Newman, Postman's sandbox and PowerShell are additional project tools, not book APIs.

## 🧩 MERN connection

Newman is an HTTP client for the Express API running on Node.js. It does not prove React browser integration or CORS. MongoDB supplies the data behind the routes.

## ⚠️ Common trap

Do not run all 93 requests blindly: IDs, singleton configuration, permissions and deletion order need preparation. The earlier isolated 90-request run used a temporary database that was removed; this smoke command does not recreate it.

## 🌐 Web culture

Collections are executable API documentation. A smoke test is a small first check, while a journey follows connected business steps.

## 🧪 Five-minute check

Explain `-e`, `--folder` and why a 401 can pass. Run smoke and save only its sanitized results. **Status: pending learner replay.**

## 🔗 Related learning

- [Docker diagnosis](docker-compose-terminal.md)
- [Requests versus assertions](api-assertions-and-negative-tests.md)
- [Fixtures and secrets](api-environments-and-fixtures.md)

> ✅ **Remember:** select a folder, satisfy its prerequisites, then read failures and skips.
