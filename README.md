# WeInc MCP Server

Official [Model Context Protocol](https://modelcontextprotocol.io) server for [WeInc](https://we.inc) — the AI website builder with flat pricing. Manage your WeInc organization from Claude, Cursor, or any MCP client: projects, publishing, custom domains, and previews.

**Hosted remote server** — nothing to install or run.

- **Endpoint:** `https://my.we.inc/api/mcp` (Streamable HTTP)
- **Auth:** Bearer token using your organization API key (`wk_...`) from the [WeInc dashboard](https://my.we.inc)
- **Registry:** listed on the [official MCP registry](https://registry.modelcontextprotocol.io) as `io.github.umairalisadaqat/weinc`
- **API docs:** https://my.we.inc/docs/api

## Quick start (Claude Code)

```bash
claude mcp add weinc --transport http https://my.we.inc/api/mcp --header "Authorization: Bearer wk_YOUR_KEY"
```

## Quick start (Cursor / other clients)

```json
{
  "mcpServers": {
    "weinc": {
      "url": "https://my.we.inc/api/mcp",
      "headers": { "Authorization": "Bearer wk_YOUR_KEY" }
    }
  }
}
```

## Tools (10)

Organization management: list/inspect projects, publish sites, manage custom domains, and generate previews. Site *generation* tools are intentionally excluded from the org-key scope — generation requires per-user embed tokens (see the [OEM API docs](https://my.we.inc/docs/api)).

## About WeInc

[WeInc](https://we.inc) generates complete production websites (React, hosted, custom domains) from a prompt. Flat monthly pricing — no token metering, failed generations never billed — plus white-label for agencies.
