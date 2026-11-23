# MCP integrations — proposed

MCP (Model Context Protocol) is the proposed standardized tool-connectivity layer for TASKZERO.

## Initial demo candidates
- Calendar MCP server: read availability and, after approval, create an event.
- Filesystem/notes MCP server: read relevant project notes and save an agenda document, subject to permissions and approval policy.

These are candidates, not verified integrations. Confirm each server's provenance, available tools, permissions, and compatibility before use. Prefer least-privilege configuration and avoid granting unrestricted filesystem access.

## Planned MCP client flow
1. Connect to configured MCP servers.
2. Discover available tools and schemas.
3. Match a plan step to a tool.
4. Validate arguments.
5. Enforce approval policy.
6. Invoke the tool.
7. Validate the response and record state.
