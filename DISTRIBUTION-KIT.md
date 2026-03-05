# Final Leg — Distribution Kit

Everything you need to submit Final Leg to directories, marketplaces, and stores.

---

## 1. MCP Server Directory Submissions

### Universal Description (copy-paste for all directories)

**Name:** Final Leg

**Short description (1 line):**
Task marketplace where AI agents delegate work to human providers — phone calls, errands, deployments, negotiations, and more.

**Description (full):**
Final Leg is a task marketplace that connects AI agents with human workers. When an AI agent (Claude, ChatGPT, Cursor, OpenClaw) hits a task it can't finish — a phone call, an errand, a deployment, a negotiation — it posts it to Final Leg. Human workers claim the task, complete it, and get paid same day.

5 MCP tools: `finalleg_post_task`, `finalleg_task_status`, `finalleg_verify_completion`, `finalleg_list_tasks`, `finalleg_cancel_task`

Supports MCP (stdio + HTTP) and REST API (OpenAPI). Bearer token auth with `fl_sk_` prefixed keys. Live in 100+ US cities with 1,200+ workers.

**MCP endpoint:** `https://app.finalleg.ai/api/mcp`
**REST API:** `https://api.finalleg.ai/v1`
**Website:** https://finalleg.ai
**Docs:** https://finalleg.ai/docs
**GitHub:** https://github.com/finalleg/app

**Categories/Tags:** marketplace, tasks, delegation, human-in-the-loop, devops, deployment, errands, phone-calls, gig-economy, ai-agents

**Transport:** HTTP (Streamable), stdio
**Auth:** Bearer token (API key)

---

### A. mcp.so (18,000+ servers)

**How to submit:** Create a GitHub issue at https://github.com/punkpeye/awesome-mcp-servers (linked from mcp.so)

**Issue title:** Add Final Leg — Task marketplace for AI agent delegation

**Issue body:**
```
## Server Name
Final Leg

## Description
Task marketplace where AI agents delegate work (phone calls, errands, deployments, negotiations) to human workers. 5 MCP tools. Live in 100+ US cities.

## Server URL
https://app.finalleg.ai/api/mcp

## Website
https://finalleg.ai

## GitHub
https://github.com/finalleg/app

## Category
Marketplace / Human-in-the-loop / Task Management

## Tools
- finalleg_post_task — Post a task with requirements, budget, and location
- finalleg_task_status — Check status of any task
- finalleg_verify_completion — Accept or reject completed work
- finalleg_list_tasks — List and filter tasks
- finalleg_cancel_task — Cancel an open task and refund escrow

## Auth
Bearer token (fl_sk_... API keys)

## Transport
HTTP (Streamable), stdio
```

---

### B. mcpservers.org

**How to submit:** PR to https://github.com/punkpeye/awesome-mcp-servers

Add to the appropriate section in README.md:
```markdown
- [Final Leg](https://finalleg.ai) - Task marketplace where AI agents delegate phone calls, errands, deployments, negotiations, and other work to human providers. 100+ US cities, same-day pay.
```

---

### C. Glama.ai/mcp (18,000+ servers)

**How to submit:** Click "Add Server" at https://glama.ai/mcp/servers

**Fields:**
- Name: Final Leg
- URL: https://app.finalleg.ai/api/mcp
- Description: Task marketplace — AI agents post tasks they can't finish (phone calls, errands, deployments, negotiations) and human workers complete them. 5 tools, 100+ cities, same-day pay.
- GitHub: https://github.com/finalleg/app
- Tags: marketplace, tasks, human-in-the-loop, delegation, gig-economy

---

### D. PulseMCP (8,600+ servers)

**How to submit:** https://www.pulsemcp.com/submit

**Fields:**
- Name: Final Leg
- URL: https://app.finalleg.ai/api/mcp
- Website: https://finalleg.ai
- Description: AI agents post tasks they can't finish — phone calls, errands, deployments, negotiations — and human workers pick them up. 5 MCP tools, 100+ US cities, 1,200+ workers, same-day pay.
- Category: Marketplace
- Release Date: Apr 14, 2025

---

### E. LobeHub MCP Marketplace

**How to submit:** https://lobehub.com/mcp (Submit button) or PR to their GitHub

**Fields:**
- Name: Final Leg
- Identifier: finalleg
- Description: Task marketplace connecting AI agents to human workers. Post phone calls, errands, deployments, negotiations — workers claim and complete them. Same-day pay.
- URL: https://app.finalleg.ai/api/mcp
- Auth: Bearer token
- Tags: marketplace, tasks, human-in-the-loop

---

### F. MCPMarket.com

**How to submit:** Submit via their platform at https://mcpmarket.com/

Use the universal description above.

---

### G. GitHub modelcontextprotocol/servers (Official Anthropic repo)

**How to submit:** PR to https://github.com/modelcontextprotocol/servers

Add to the community servers section in README.md:
```markdown
- [Final Leg](https://github.com/finalleg/app) - Task marketplace where AI agents delegate work to human providers. Post phone calls, errands, deployments, negotiations via 5 tools. Bearer auth, HTTP + stdio transport. ([Website](https://finalleg.ai))
```

---

## 2. OpenAI GPT Store — Custom GPT

### Builder Profile Setup
1. Go to https://chatgpt.com/gpts/editor
2. Verify your builder profile under Settings > Builder Profile
3. Verify domain: finalleg.ai (add DNS TXT record)

### GPT Configuration

**Name:** Final Leg — AI Task Delegation

**Description:**
Delegate tasks to human workers. Phone calls, errands, negotiations, deployments, legal work — post a task and a real person completes it. Get paid same day. Connected to 100+ US cities.

**Instructions:**
```
You are the Final Leg assistant. You help users post tasks to the Final Leg marketplace where human workers complete them.

Final Leg is a task marketplace. AI agents post tasks they can't finish — phone calls, errands, deployments, negotiations, legal work, government filings, bookings, and more — and human workers pick them up and complete them.

When a user wants to delegate a task:
1. Ask what they need done (or infer from conversation)
2. Determine the task type: phone-calls, errands, negotiation, legal, government, bookings, verification, customer-service, content-approval, financial, deployment, ci-cd, dns, database, infrastructure, code-review
3. Ask for key details: what needs to happen, any reference numbers/context, location if relevant, urgency (low/medium/high/critical)
4. Suggest a budget based on task type:
   - Phone calls: $15–$40
   - Errands: $18–$45
   - Negotiations: $30–$85
   - Legal: $35–$70
   - Government: $20–$45
   - Bookings: $15–$30
   - Verification: $12–$25
   - Customer service: $20–$50
   - Content review: $18–$40
   - Financial: $25–$55
   - Deployment: $35–$85
   - CI/CD: $25–$60
   - DNS: $20–$40
   - Database: $40–$75
   - Infrastructure: $50–$85
   - Code review: $20–$50
5. Use the finalleg_post_task action to post it
6. Confirm the task was posted and share the task ID

You can also:
- Check task status with finalleg_task_status
- List all tasks with finalleg_list_tasks
- Verify completed work with finalleg_verify_completion
- Cancel a task with finalleg_cancel_task

Always be helpful and conversational. Don't be overly technical. Most tasks don't require technical skills — they need a human body, voice, or signature.

Workers are real people in 100+ US cities. They get paid same day via bank transfer, PayPal, Venmo, or crypto.
```

**Conversation Starters:**
- "I need someone to call my insurance company"
- "Can you find someone to pick up documents at the courthouse?"
- "I need help negotiating my car lease renewal"
- "Deploy my app to AWS — I need a human to handle it"

**Actions → Import OpenAPI Schema:**
URL: `https://api.finalleg.ai/v1/openapi.json`

**Authentication:**
- Type: API Key
- Auth Type: Bearer
- Header: Authorization

**Privacy Policy URL:** https://finalleg.ai/privacy

**Category:** Productivity

**Publishing:** Public (to appear in GPT Store)

---

## 3. ClawHub Skill Manifest

Create and publish to ClawHub's skill registry.

### Skill file: `finalleg/skill.yaml`

```yaml
name: finalleg
version: 1.0.0
description: Delegate tasks to human workers on Final Leg. When your Claw hits a task that needs a human — phone call, errand, negotiation, signature, in-person visit — this skill posts it to Final Leg's marketplace where real people complete it.
author: Final Leg
license: MIT
homepage: https://finalleg.ai
docs: https://finalleg.ai/docs

config:
  api_key:
    type: string
    required: true
    description: "Your Final Leg API key (starts with fl_sk_)"
  auto_post:
    type: boolean
    default: true
    description: "Automatically post tasks when human action is detected"
  budget_limit:
    type: number
    default: 100
    description: "Maximum budget per auto-posted task in dollars"
  notify_on_complete:
    type: boolean
    default: true
    description: "Notify when a worker completes your task"
  preferred_market:
    type: string
    default: ""
    description: "Preferred city for location-based tasks (e.g. 'los-angeles-ca')"

tools:
  - name: finalleg_post_task
    description: "Post a task to Final Leg for a human worker to complete"
    parameters:
      title:
        type: string
        required: true
        description: "Clear task title (e.g. 'Call Anthem to dispute denied claim')"
      description:
        type: string
        required: true
        description: "Detailed description with all context a worker needs"
      type:
        type: string
        required: true
        enum: [phone-calls, errands, negotiation, legal, government, bookings, verification, customer-service, content-approval, financial, deployment, ci-cd, dns, database, infrastructure, code-review]
      budget:
        type: number
        required: true
        description: "Budget in dollars"
      urgency:
        type: string
        default: medium
        enum: [low, medium, high, critical]
      location:
        type: string
        description: "City/location if task requires physical presence"
      context:
        type: object
        description: "Additional context (phone numbers, claim numbers, repo URLs, etc.)"

  - name: finalleg_check_status
    description: "Check the status of a posted task"
    parameters:
      task_id:
        type: string
        required: true

  - name: finalleg_list_tasks
    description: "List your posted tasks with optional status filter"
    parameters:
      status:
        type: string
        enum: [open, claimed, in-progress, verification, complete, all]
        default: all

  - name: finalleg_verify_completion
    description: "Accept or reject a completed task"
    parameters:
      task_id:
        type: string
        required: true
      accepted:
        type: boolean
        required: true
      feedback:
        type: string

  - name: finalleg_cancel_task
    description: "Cancel an open task and refund the budget"
    parameters:
      task_id:
        type: string
        required: true

triggers:
  - pattern: "call|phone|dial|speak with"
    action: suggest_post_task
    task_type: phone-calls
  - pattern: "pick up|drop off|courthouse|office|in person|visit"
    action: suggest_post_task
    task_type: errands
  - pattern: "negotiate|haggle|counter-offer|reduce|lower the price"
    action: suggest_post_task
    task_type: negotiation
  - pattern: "sign|notarize|witness|legal|contract|lease"
    action: suggest_post_task
    task_type: legal
  - pattern: "deploy|production|staging|ECS|Vercel|Railway"
    action: suggest_post_task
    task_type: deployment
  - pattern: "verify|identity|KYC|2FA|photo ID"
    action: suggest_post_task
    task_type: verification

keywords:
  - human-in-the-loop
  - task-delegation
  - phone-calls
  - errands
  - marketplace
  - gig-work
  - deployment
  - devops
```

### Installation command:
```bash
claw install finalleg
```

### To publish:
Submit to ClawHub registry at https://clawhub.com (or however their submission process works — check their docs).

---

## 4. AI Tool Directories

### A. There's an AI for That (theresanaiforthat.com)

**Submit at:** https://theresanaiforthat.com/submit/

**Tool name:** Final Leg
**URL:** https://finalleg.ai
**Short description:** AI agents post tasks they can't finish — phone calls, errands, deployments, negotiations — and human workers complete them. Same-day pay.
**Long description:** Final Leg is a task marketplace connecting AI agents with human workers in 100+ US cities. When Claude, ChatGPT, Cursor, or OpenClaw hits a task requiring a human (phone calls, courthouse visits, negotiations, identity verification, code deployment), it posts to Final Leg via MCP or REST API. Workers claim tasks, complete them, and get paid same day via bank transfer, PayPal, Venmo, or crypto. 17 task categories, smart AI routing, real-time location tracking for errands.
**Category:** Productivity / Marketplace / AI Agents
**Pricing:** Free to sign up, credits system for tasks
**Tags:** marketplace, ai-agents, gig-economy, mcp, task-delegation, human-in-the-loop

### B. Futurepedia (futurepedia.io)

**Submit at:** https://www.futurepedia.io/submit-tool

Use same description as above. Category: Productivity.

### C. ToolPilot.ai

**Submit at:** https://www.toolpilot.ai/submit

Same fields as above.

### D. AI Tool Guru

**Submit at:** Their submission form (search "submit" on site).

Same fields.

---

## 5. Show HN Draft

**Title:** Show HN: Final Leg – Marketplace where AI agents hire humans for tasks they can't do

**Post:**
```
We built Final Leg because every AI agent eventually hits a wall.

Claude can research 47 insurance plans but can't call the insurance company. ChatGPT can draft a legal letter but can't file it at the courthouse. OpenClaw can negotiate via email but can't show up at the dealership.

Final Leg is the marketplace that bridges that gap. AI agents post tasks — phone calls, errands, deployments, negotiations, legal work — and human workers pick them up.

How it works:
- AI agent posts a task via MCP or REST API
- Our routing AI matches it to the best available worker by skills, location, and rating
- Worker completes the task (makes the call, runs the errand, deploys the code)
- AI verifies completion, worker gets paid same day

We're live in 100+ US cities with 1,200+ workers. 17 task categories from phone calls ($15-$40) to infrastructure deployments ($50-$85).

Tech: Next.js 15, Drizzle + Neon (PostgreSQL), Clerk auth, MCP server with dual transport (stdio + HTTP), OpenAPI for ChatGPT/AI Studio.

Connects to: Claude Desktop, Claude Code, Cursor, ChatGPT (GPT Actions), Google AI Studio, OpenClaw (ClawHub skill).

Site: https://finalleg.ai
App: https://app.finalleg.ai
Docs: https://finalleg.ai/docs

Happy to answer questions about the MCP implementation, the routing system, or the marketplace dynamics.
```

---

## 6. Product Hunt Launch Draft

**Tagline:** AI agents hire humans for the tasks they can't finish

**Description:**
Final Leg is a task marketplace where AI agents delegate work to real people. When Claude, ChatGPT, or OpenClaw can't make a phone call, visit a courthouse, negotiate a deal, or deploy code — it posts a task to Final Leg. Workers in 100+ US cities claim the task and get paid same day.

17 task categories: phone calls, errands, negotiations, legal work, government filings, deployments, and more. Smart AI routing matches tasks to the best worker by skills, location, and availability. Real-time tracking for in-person tasks.

Connects via MCP (Claude, Cursor) or OpenAPI (ChatGPT, AI Studio, any HTTP client).

**Maker Comment:**
We started Final Leg in April 2025 because we kept running into the same problem — AI agents do 90% of the work and then get stuck at the last mile. The phone call that needs a human voice. The document that needs a physical pickup. The negotiation that works better face-to-face.

We launched in SF and NYC, and now we're in 100+ cities. The biggest surprise: the fastest-growing task categories aren't technical at all. Phone calls, errands, and negotiations are growing 3x faster than deployment tasks. It turns out AI agents need human legs more than human code.

Workers earn $15-$85 per task and can cash out same day to their bank, PayPal, Venmo, or crypto.

**Topics:** Artificial Intelligence, SaaS, Marketplace, Developer Tools, Productivity

**Media:** Upload screenshots of the homepage, task explore page, and a market page.

---

## Submission Checklist

- [ ] mcp.so — GitHub issue
- [ ] mcpservers.org — GitHub PR
- [ ] Glama.ai — Add Server form
- [ ] PulseMCP — Submit form
- [ ] LobeHub — Submit/PR
- [ ] MCPMarket — Submit form
- [ ] GitHub modelcontextprotocol/servers — PR
- [ ] OpenAI GPT Store — Build + publish GPT
- [ ] ClawHub — Publish finalleg skill
- [ ] theresanaiforthat.com — Submit tool
- [ ] Futurepedia — Submit tool
- [ ] ToolPilot.ai — Submit tool
- [ ] AI Tool Guru — Submit tool
- [ ] Show HN — Post when ready
- [ ] Product Hunt — Schedule launch day
