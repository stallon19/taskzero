# TASKZERO — 24-hour MVP roadmap

> Proposed hackathon build plan. This is a target plan, not a claim of completion.

## Scope guardrail
Demonstrate one end-to-end workflow with a small number of compatible tools. Avoid building a universal connector catalog or multiple incomplete workflows.

| Time | Focus | Planned outcome |
|---|---|---|
| 0–6 h | Foundation & planning | API skeleton, structured planner output, MCP client connection |
| 6–14 h | Tools & approval | Connect chosen calendar and notes tools; approval flow for writes |
| 14–19 h | State & dashboard | Status tracking, persistence, validation, responsive dashboard |
| 19–24 h | Integration & polish | End-to-end demo, error paths, optional voice briefing, pitch/demo readiness |

## MVP acceptance checklist
- [ ] Accept a natural-language goal in the UI.
- [ ] Generate a structured, schema-valid plan.
- [ ] Show the plan and step statuses to the user.
- [ ] Discover/invoke a limited set of tools through MCP.
- [ ] Require explicit approval before external write operations.
- [ ] Record step states and failures.
- [ ] Validate returned tool data before claiming completion.
- [ ] Provide a concise final report.
- [ ] Demo a failure or rejected action safely.
- [ ] Keep API keys and secrets out of repository history.

## Risks and mitigations
- **MCP server availability:** test candidate servers early; keep a deterministic demo fixture as fallback and clearly label it.
- **Malformed planner output:** validate with Pydantic; request a revised plan or fail safely.
- **Unexpected side effects:** approval gate, least-privilege credentials, and explicit action preview.
- **Latency:** timeouts, bounded retries, clear pending/error UI.
- **Voice integration time:** optional; prioritize the core task flow first.
