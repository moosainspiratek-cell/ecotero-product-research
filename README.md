# ecotero-product-research

Workspace for Claude Code product research against the Ecotero Command Center.

## Layout

```
.mcp.json              MCP server: ecotero-command-center (HTTP)
.claude/settings.json  Enables ecotero-command-center for this project
CLAUDE.md              Rules for the research agent
```

The file names matter. Claude Code only reads `.mcp.json` (leading dot, repo root) and
`.claude/settings.json`; a file named `mcp.json` or a root `settings.json` is ignored and the
server never connects.

## Setup

- The cloud environment needs the secret `ECOTERO_AGENT_KEY` (the `design-team-claude-code`
  agent key). `.mcp.json` reads it as `Bearer ${ECOTERO_AGENT_KEY}`; never paste the key into the file.
- MCP servers load when a session starts. After changing either config file, start a new session
  and run `/mcp` to confirm `ecotero-command-center` shows as connected.
