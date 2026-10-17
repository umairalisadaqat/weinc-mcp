# Installing the WeInc MCP server

WeInc is a hosted remote MCP server. There is nothing to clone, build or run locally, and no API key to paste.

1. Add a remote server named `weinc` with URL `https://my.we.inc/api/mcp` using the Streamable HTTP transport. For Cline, add this to `cline_mcp_settings.json`:

```json
{
  "mcpServers": {
    "weinc": {
      "type": "streamableHttp",
      "url": "https://my.we.inc/api/mcp"
    }
  }
}
```

2. Confirm the connection by listing tools. `initialize` and `tools/list` work without signing in; you should see 15 tools such as `start_website`, `find_templates` and `my_websites`.
3. The first time a tool needs the user's account, the client opens a WeInc OAuth sign-in in the browser. The user signs in (or creates a free account at https://we.inc). No other setup is needed.

Nothing is built, changed or charged until the user confirms it inside WeInc.
