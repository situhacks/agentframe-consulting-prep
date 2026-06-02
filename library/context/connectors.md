# Connectors — Composio

**Composio is this system's all-in-one tool hub.** One connection exposes 100+ external tools, so the agent
can reach your real accounts when a task benefits from it — instead of you copy-pasting between apps.

**Optional.** Everything in this system works without it. Composio just adds reach to the outside world.

## The headline use case: markdown → Google Doc
Draft your CV/cover letter as markdown, then push it straight to an **editable Google Doc** to do final edits.
Tool: `GOOGLEDOCS_CREATE_DOCUMENT_MARKDOWN` (params: `title`, `markdown_text`). The `doc-export` skill uses this.
**Verified working** — markdown headings/bullets render as proper Google Doc formatting.

## What else it unlocks (consulting prep)
- **Gmail** — draft a networking / cold-outreach email to a recruiter or alum, in your voice, ready to send.
- **Google Calendar** — check availability before proposing coffee-chat / interview times.
- **Google Drive / Docs** — pull a JD from Drive; create the editable CV/letter Doc.

## Setup (once)

**Option A — Composio MCP server in your coding agent (recommended):**
Add Composio as an MCP server so its tools appear natively in the agent.
- Server config (Streamable HTTP): URL `https://connect.composio.dev/mcp`, with your API key as the auth header.
- Get an API key (an `ak_…` key) from the Composio dashboard.
- In the Composio dashboard, **connect the apps you want** (Google Docs, Gmail, Calendar) — this is the OAuth step.

**Option B — Composio Python SDK (what this repo's smoke test used):**
```python
from composio import Composio
c = Composio(api_key="ak_…")                 # from the dashboard
# one-time per app: find/confirm an auth config for the toolkit, then link your user (returns an OAuth URL):
req = c.connected_accounts.link(user_id="<you>", auth_config_id="<ac_… for googledocs>")
print(req.redirect_url)                       # open it, authorize Google
# after authorizing, the connection is ACTIVE and tools work:
c.tools.execute("GOOGLEDOCS_CREATE_DOCUMENT_MARKDOWN",
                user_id="<you>",
                arguments={"title": "...", "markdown_text": "..."},
                dangerously_skip_version_check=True)
```
Put your key in `.env` (`COMPOSIO_API_KEY=ak_…`) — `.env` is gitignored.

## How the agent should use it
- Treat Composio as available-if-connected. Before reaching an external tool, check what's connected; if nothing
  useful is, do the task locally (e.g. write the email as a draft file, or export a local .docx) and tell the user.
- Draft-first / read-first: prepare drafts and check info; don't send or change anything without the user's ok.
