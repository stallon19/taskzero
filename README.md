# TASKZERO

**From Intention to Execution.**  
*One instruction. Multiple tools. One completed task.*

TASKZERO is a proposed AI-powered task execution agent that turns natural-language goals into structured workflows, connects to compatible external tools through the **Model Context Protocol (MCP)**, pauses for user approval before sensitive write actions, and verifies tool responses before reporting outcomes.

> **Project status:** Ideathon proposal / planned MVP. This repository contains the concept, architecture, workflow, and roadmap. Features and integrations described here are proposed—not implemented or deployed.

## The problem
AI assistants can help users plan and draft, but coordinating a multi-step task across calendars, documents, and other tools still often requires manual context switching. TASKZERO proposes a workflow-oriented agent that takes a goal through planning, tool discovery, approval, execution, and verification.

## Proposed workflow
**UNDERSTAND → PLAN → CONNECT → EXECUTE → VERIFY → REPORT**

1. Understand the natural-language goal.
2. Create a structured plan and dependency graph.
3. Discover suitable tools through connected MCP servers.
4. Pause for explicit approval before sensitive/external write actions.
5. Execute approved tool calls and track state.
6. Validate responses and report completed, pending, or failed steps.

## Example
> “Organize a project meeting for our team next week. Check everyone's availability, find a suitable time, prepare an agenda based on our latest project updates, schedule the meeting and share the agenda.”

TASKZERO would plan the steps, consult compatible calendar and notes tools, prepare the proposed event and agenda, ask for approval before writes, then validate the tool responses and report the outcome.

## Proposed MVP
- Web dashboard showing a task and execution step statuses
- Backend planner that returns a schema-validated task plan
- MCP client connected to a limited set of compatible servers
- Approval gate before external write operations
- Execution-state tracking
- Basic response validation and completion report
- Optional ElevenLabs text-to-speech completion briefing, if time permits

## Proposed technology stack
| Layer | Proposed technology | Purpose |
|---|---|---|
| Frontend | Next.js / React | Task input, workflow visualization, approval UI, status dashboard |
| Backend | Python / FastAPI | API and orchestration controller |
| Planner | LLM API with structured output | Goal interpretation and task decomposition |
| Tool connectivity | MCP client / SDK | Discover and invoke compatible tools through MCP |
| State | SQLite + Pydantic validation | Execution state and schema validation |
| Voice | ElevenLabs API (optional MVP) | Spoken status briefing / TTS |

## Safety and execution principles
- Explicit confirmation before sensitive external write actions.
- Validate structured plans before execution.
- Treat tool outputs as data, not instructions.
- Track execution state and distinguish success, failure, and pending steps.
- Use timeouts and bounded retries; never claim completion without evidence from tool responses.
- Keep secrets out of Git; use environment variables and local secret storage.

## Repository map
```text
taskzero/
├── README.md
├── LICENSE
├── .gitignore
├── docs/                 # Architecture, workflow, MVP roadmap
├── frontend/              # Planned web console
├── backend/               # Planned orchestration API
├── mcp/                   # MCP integration notes
├── assets/                # Logo and diagrams
└── presentation/           # Ideathon pitch deck
```

## Team
**MIDNIGHT BUILDERS** · Sapthagiri NPS University  
**wHACKiest 2026 · Track 1 — Make MCP Matter · Team ID: 041b6d40**
- Stallon S (Lead) — 24SUUBECS2145
- Sudarshan K Rathod — 24SUUBECS2148
- Suhas G — 24SUUBECS2158
- Suraj ND — 24SUUBECS2186

## Current stage
This is a blueprint repository for the ideathon. The code directories contain planning notes and placeholders until the implementation phase begins. See [MVP roadmap](docs/mvp-roadmap.md).
