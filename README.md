# WeInc MCP Server

Official [Model Context Protocol](https://modelcontextprotocol.io) server for [WeInc](https://we.inc), the AI website builder. Build and manage websites from Claude, Cursor or any MCP client: describe a business to get a link that starts the build, browse templates, see your websites and whether they are published, and prepare changes that open in the WeInc editor ready to send. Agency accounts can also manage clients, client sites, preview links and analytics.

**Hosted remote server**, nothing to install or run.

- **Website:** https://we.inc
- **Endpoint:** `https://my.we.inc/api/mcp` (Streamable HTTP)
- **Auth:** OAuth 2.1. Your client opens a WeInc sign-in the first time you use a tool. Tool discovery (`initialize`, `tools/list`) works without signing in.
- **Registry:** listed on the [official MCP registry](https://registry.modelcontextprotocol.io) as `io.github.umairalisadaqat/weinc`

Nothing is built or changed until you confirm it in WeInc.

## Quick start (Claude Code)

```bash
claude mcp add weinc --transport http https://my.we.inc/api/mcp
```

## Quick start (Cursor / other clients)

```json
{
  "mcpServers": {
    "weinc": { "url": "https://my.we.inc/api/mcp" }
  }
}
```

## Tools

- **Websites:** `start_website`, `find_templates`, `my_websites`, `website_details`, `request_change`
- **Agency / projects:** `list_projects`, `create_project`, `get_project`, `update_project`, `get_preview_urls`
- **Agency / clients and plans:** `list_clients`, `create_client`, `list_templates`, `list_plans`, `get_analytics`

## About WeInc

[WeInc](https://we.inc) generates complete production websites (hosted, custom domains) from a prompt, with white-label for agencies.
