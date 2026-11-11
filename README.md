# Moxboard MCP server

Moxboard is a simple kanban board for small teams, with one price per workspace by team size instead of per-user billing.

This is the hosted MCP server for [Moxboard](https://moxboard.app). Connect Claude (or any MCP client that supports sign-in with OAuth) to ask about your work and create or update tasks by chat.

**Server address:** `https://app.moxboard.app/mcp` (Streamable HTTP, OAuth)

Included on every Moxboard plan, Free included.

## Connect

**Claude (web, desktop and mobile):** Settings → Connectors → Add custom connector. Name it Moxboard, paste the server address, click Add, then Connect. Sign in to Moxboard, choose the workspaces Claude can use and whether it can *Read and edit* or *Read only*, and click Allow.

**Claude Code:**

```bash
claude mcp add --transport http moxboard https://app.moxboard.app/mcp
```

Then type `/mcp`, choose `moxboard` and sign in.

## What it can do

- List your workspaces, projects, columns and people.
- Search tasks by text, person, column, label or due date, and read a task with its subtasks and comments.
- Summarise a project: open, overdue, done in a period, work per person.
- With *Read and edit*: create tasks and subtasks (up to 50 at a time), change titles, descriptions, dates, priority, labels and assignee, move tasks between columns, mark them done and comment.

## What it can't do

- Delete tasks, projects or comments.
- Invite or remove people, change roles, billing, project privacy or settings.
- Open attachments (it only sees their names).

## Safe by design

- Claude works as you: it only sees what you can see. Private projects you're not in stay hidden, and guests stay limited to their projects.
- Every change appears in the task history as made by you, via Claude.
- Disconnect at any time: account menu → Integrations → Disconnect. Workspace owners and admins can turn AI apps off for the whole workspace.
- Task text is treated as information, never as instructions.
- Moxboard data is hosted in the EU.

## Links

- Website: https://moxboard.app
- App: https://app.moxboard.app
- Help: https://help.moxboard.app/claude
- Company: FTU, Lda — Porto, Portugal
