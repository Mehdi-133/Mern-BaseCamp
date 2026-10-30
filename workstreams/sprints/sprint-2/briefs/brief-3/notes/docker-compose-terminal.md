# 🐳 Docker Compose: start, inspect, diagnose

> 🟡 **In progress — 30 October 2026.** Commands discussed and startup logs supplied by the learner; independent explanation still needs checking.
>
> 🧠 **Big idea:** Docker runs the API and MongoDB; inspect their state before sending API tests.

## 🔑 Commands to remember

Run from the LMS project folder, not BaseCamp:

```powershell
cd C:\Users\LENOVO\Desktop\fondations_API_LMS
docker info
docker compose up -d --build
docker compose ps
docker compose logs --tail 50 api
```

| Command | Purpose | Changes anything? |
| --- | --- | --- |
| `docker info` | Shows Docker client/server information; check that the engine responds | Read-only |
| `docker compose up -d --build` | Builds images and creates/starts services; `-d` runs in the background | Yes: containers/images, and possibly a new volume |
| `docker compose ps` | Shows service/container state and published ports | Read-only |
| `docker compose logs --tail 50 api` | Reads the most recent 50 lines from the `api` service | Read-only; it does not start or restart the API |

`api` is the Compose service name; `lms-api` is its configured container name. `--build` rebuilds the API image; it does not promise the process will stay healthy. `up` does not run the seed in this project.

## 🛠️ Troubleshooting order

1. Named-pipe error mentioning `dockerDesktopLinuxEngine`: the Docker CLI cannot reach the selected Linux engine. Open Docker Desktop and wait for its engine; if needed, restart it and recheck `docker info`. A context/configuration problem is another possibility if the engine is running.
2. `ECONNREFUSED 127.0.0.1:3000`: no server accepted that connection. Check `docker compose ps`, then API logs; do not debug response JSON before there is a response.
3. `SEED_DEMO_PASSWORD` unset: a separate Compose interpolation warning. Public smoke needs no account password. Do not run the seed as a connection fix: it can reset demo passwords and replace matching data.
4. Learner supplied logs showing `MongoDB connected` and `Server running on port 3000`. This proves reported startup at that time, not successful host requests, all endpoints, or a seed run.

## 📖 Eloquent JavaScript foundation

- **Chapter 8, Bugs and Errors, printed pp. 135–136:** repeat checks and use evidence to locate a failure rather than guessing.
- **Chapter 18, HTTP and Forms, printed pp. 317–318:** a client first connects to a server, then exchanges an HTTP request/response.
- **Boundary:** the local book was consulted; it does not teach Docker Compose or Windows named pipes.

## 🧩 MERN connection

- **Node.js/Express:** the API process listens on container port 3000, published to host port 3000.
- **MongoDB:** Compose publishes host port 27018 to Mongo's container port 27017. Inside Compose the API uses `mongo:27017`, not host `localhost:27018`.

## ⚠️ Common trap

Reading logs cannot repair a stopped engine. A running container is also not proof that every business rule works. Avoid `docker compose down -v` as routine troubleshooting because `-v` can remove stored database volumes.

## 🌐 Web culture

Teams inspect infrastructure, process startup and HTTP behavior as separate checkpoints. Share relevant errors, never the whole secret-bearing environment.

## 🧪 Five-minute check

Explain why `logs` cannot fix a stopped API and name the first command to use for the engine error. **Status: not attempted.**

## 🔗 Related learning

- [Newman commands](postman-newman-terminal.md)
- [Delivery evidence](postman-frontend-handoff.md)

> ✅ **Remember:** engine → containers → API startup → HTTP checks.
