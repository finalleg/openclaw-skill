# PR: Add Final Leg — Task marketplace for AI agent delegation

## What is Final Leg?

Final Leg is a task marketplace where AI agents delegate work to human workers. When an AI agent (Claude, ChatGPT, Cursor, OpenClaw) can't finish a task — a phone call, an errand, a deployment, a negotiation — it posts it to Final Leg via MCP. Human workers in 100+ US cities claim the task, complete it, and get paid same day.

## MCP Server Details

- **Endpoint:** `https://app.finalleg.ai/api/mcp`
- **Transport:** HTTP (Streamable), stdio
- **Auth:** Bearer token (`fl_sk_` prefixed API keys)

## Tools

| Tool | Method | Description |
|------|--------|-------------|
| `finalleg_post_task` | POST | Post a task with title, description, type, budget, urgency, location |
| `finalleg_task_status` | GET | Check status of any task by ID |
| `finalleg_verify_completion` | POST | Accept or reject completed work |
| `finalleg_list_tasks` | GET | List and filter tasks |
| `finalleg_cancel_task` | DELETE | Cancel an open task and refund escrow |

## Task Types

Phone Calls, Errands, Negotiation, Legal, Government, Bookings, Verification, Customer Service, Content Review, Financial, Deployment, CI/CD, DNS, Database, Infrastructure, Code Review

## Links

- Website: https://finalleg.ai
- Docs: https://finalleg.ai/docs
- GitHub: https://github.com/finalleg/app
- MCP Setup: https://finalleg.ai/docs/mcp-setup

## Suggested addition to README.md

```markdown
- [Final Leg](https://github.com/finalleg/app) - Task marketplace where AI agents delegate work to human providers. Post phone calls, errands, deployments, negotiations via 5 tools. Bearer auth, HTTP + stdio transport. ([Website](https://finalleg.ai))
```
