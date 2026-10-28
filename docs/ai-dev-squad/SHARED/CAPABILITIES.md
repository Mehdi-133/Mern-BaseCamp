# 🔌 Capability and permission audit

Snapshot: **28 October 2026**, this local Codex chat. Tools listed by the session are not proof of account-wide capabilities.

| Capability | Evidence | Status / limit |
| --- | --- | --- |
| Local workspace | Repository files/Git read; focused documentation writes | Available inside granted roots; protected config directories need approval |
| Codex | Local CLI `0.163.0-alpha.11.2`; actual spawn/message tools | Four delegated roles ran; four concurrent slots include parent |
| Persistent agents | No Workspace Agents provisioning tool exposed | Not provisioned; reusable local definitions and explicit handoffs are the fallback |
| Jira / Confluence | Accessible-resource call succeeded | One connected site: `mehdikarbitou-1769453505855.atlassian.net` |
| LMS Jira | `project = FAL ORDER BY updated DESC`, max 3 | Zero issues; target project's site access unresolved; no Jira writes |
| Google Calendar | Primary-account calendar listing succeeded | Owner role returned for primary calendar; no events read/written |
| Gmail | Authenticated profile call succeeded | Connection responded; message access/sending not tested or authorized |
| Google Drive | Shared-drive listing returned empty array | API responded; no claim about personal Drive files or write access |
| Notion | Existing Learning Hub fetched | Read verified; sync outcome recorded in current status |
| Figma / Canva | Relevant tools exposed | Account/file access and editing not tested; need an authorized destination |
| Images | Built-in generation tool exposed | Generated asset results and visual review tracked separately |
| Video editing | Descript tools exposed | Not exercised; no video produced |
| Git | Local branch/status/HEAD read successfully | Remote auth/push/CI not verified; GitHub CLI not found in PATH |
| Node.js | Four LMS files passed syntax checks | Application/runtime suite unexecuted |
| Docker / databases / IDEs | Tool availability not tested | Prior session evidence is not a new live check |
| Postman / Apidog / Maven / JUnit | Not exercised | Installed Postman CLI is user-provided context, not a test result |
| Scheduling | Desktop automation creation tool exposed | No task created; exact approval required by this request |

## 🔐 Role permission matrix

| Role | Routine authorized work | Approval boundary |
| --- | --- | --- |
| Ayoube | Read relevant tasks/calendar; draft plans/handoffs | Significant dates/assignments/calendar writes, external messages, automations |
| Walid | Read/edit scoped repo, safe builds/checks, propose branches/commits | Git publication, destructive commands, production changes, protected merges |
| Annas | Read diffs/logs, isolated tests, QA reports | Shared database mutation, deployments, protection changes |
| Reda | Draft design/assets, visual review, authorized service drafts | Publishing and external distribution |

These are operating rules, not independently enforced per-role sandboxes. All subagents inherit the parent session's tools and controls. Minimize context and assign explicit scopes.

## 📚 Official reference

[Custom agents and inheritance](https://learn.chatgpt.com/docs/agent-configuration/subagents) describes project TOML definitions and parent-controlled permissions. This session demonstrates delegation, not account eligibility for persistent Workspace Agents.
