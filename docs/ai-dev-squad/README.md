# 🤝 AI DEV SQUAD

> 🟡 Local reusable team kit prepared on 28 October 2026. Four real delegated reviews completed; persistent independent services have not been provisioned.

You own goals, decisions and delivery approval. **Ayoube** coordinates; **Walid** engineers; **Annas** verifies; **Reda** designs. English by default, French freely, Darija when requested. Identities are fictional AI roles.

## 🚀 Talk to your team

In a chat with this repository open, use:

```text
Read docs/ai-dev-squad/README.md and SHARED/TEAM_RULES.md.
Ayoube, coordinate a read-only review of the LMS using PROJECTS/lms/CONTEXT.md.
Delegate independent engineering, QA and design reviews to Walid, Annas and Reda.
Combine their evidence into one handoff. Do not change application code.
```

Or address one role: **“Walid, review this module”**, **“Annas, test this feature”**, **“Reda, prepare a design concept”**, **“Ayoube, organize my day.”** Naming a role selects instructions; actual delegation must be visible in tool activity.

Read the matching [profile](AGENTS/README.md) before working. Runtime-ready TOML definitions are in [configs/](configs/README.md). They inherit the parent's selected model and permissions. A saved definition is not a continuously running worker. Use explicit handoffs across chats; don't assume shared conversation memory.

## 🧭 Start here

| Need | Source |
| --- | --- |
| Roles and commands | [Profiles](AGENTS/README.md) |
| Coordination and approval boundaries | [Team rules](SHARED/TEAM_RULES.md) |
| Tools actually checked | [Capability audit](SHARED/CAPABILITIES.md) |
| Sources of truth and project isolation | [Project registry](SHARED/PROJECT_REGISTRY.md) |
| Ready-to-use context transfer | [Handoff template](SHARED/HANDOFFS.md) |
| Setup status and limitations | [Current status](SHARED/CURRENT_STATUS.md) |
| First real delegated demonstration | [LMS report](PROJECTS/lms/DEMO.md) |
| Scheduling proposals awaiting your choice | [Automations](SHARED/AUTOMATIONS.md) |
| Portraits and creative guidance | [Assets](assets/README.md) |

## 🧠 Why this works

The role defines **how to work**. Project context defines **what to work on**. A handoff carries **what was actually done and checked**. Tools execute the work; role names alone do not grant access.

Official [custom-agent documentation](https://learn.chatgpt.com/docs/agent-configuration/subagents) specifies standalone TOML files with `name`, `description` and `developer_instructions`. Project definitions belong in `.codex/agents/`; personal definitions belong in `~/.codex/agents/`. The parent session controls tool connections and permissions. Documentation checked on 28 October 2026; actual definition loading still requires a fresh-session smoke check.

## ✅ Verification boundary

Four delegated agents returned independent reports using the live LMS checkout. Four JavaScript syntax checks passed. No HTTP, email, database, CI, deployment or release result was tested. Jira story demonstration remains blocked by site access. No application code changed. The learner authorized documentation publication through the 28 October clean-push request; the setup review itself did not publish application work.
