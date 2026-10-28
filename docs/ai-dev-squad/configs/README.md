# ⚙️ Reusable Codex agent definitions

Four TOML files define `name`, `description` and `developer_instructions` using the [official standalone agent format](https://learn.chatgpt.com/docs/agent-configuration/subagents).

These are reviewable configuration sources. Copies were installed into this repository's protected `.codex/agents/` directory with filesystem approval on 28 October 2026. Personal installation under `~/.codex/agents/` is a separate choice; no global configuration changes are part of this kit. Fresh-session discovery is not yet verified.

After installation, start a fresh chat with this repository open and ask:

```text
Use the custom ayoube agent to summarize docs/ai-dev-squad/SHARED/CURRENT_STATUS.md.
Read only. Report its actual result and whether custom-agent loading succeeded.
```

Repeat with `walid`, `annas`, `reda`. If this client's runtime does not discover them, read the matching Markdown profile explicitly and delegate with those instructions. Record the fallback; don't claim the custom definition loaded.

No model override, credentials, MCP server configuration, permission override or background service is included. Profiles are shared Markdown sources; definitions direct agents to read them at runtime to avoid duplicating full rules.
