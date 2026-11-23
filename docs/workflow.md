# TASKZERO — Example Workflow

## User request
“Organize a project meeting for our team next week. Check everyone's availability, find a suitable time, prepare an agenda based on our latest project updates, schedule the meeting and share the agenda.”

## Planned steps
1. Interpret the request and identify the date window, participants, and meeting purpose. Ask for missing details when required.
2. Discover available calendar and project-notes tools through configured MCP servers.
3. Retrieve relevant project updates using permitted read operations.
4. Check participant calendar availability and propose candidate times.
5. Draft a meeting agenda from the retrieved project updates.
6. Prepare the meeting event and agenda document for review.
7. Present the exact external write actions to the user for approval.
8. If approved, create the calendar event and save/share the agenda using compatible tools and permissions.
9. Validate tool responses and update each step's state.
10. Report verified completed steps, unresolved steps, and any failures.

## Approval policy
Approval is required before external write actions such as creating or modifying a calendar event, sending invitations, sharing documents, deleting data, or overwriting files. The approval prompt should show what will happen, which account/tool will be used, and the relevant details. Rejection must prevent that action.

## Verification policy
A task is not marked completed merely because a tool call was attempted. Check the returned result and, where feasible, confirm the expected record or artifact exists. Report partial completion accurately.
