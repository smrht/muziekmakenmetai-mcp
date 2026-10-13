# Installing Muziek maken met AI in Cline

This is a hosted remote MCP server. There is nothing to clone, build or install.

Add this entry to `cline_mcp_settings.json`:

```json
{
  "mcpServers": {
    "muziekmakenmetai": {
      "type": "streamableHttp",
      "url": "https://muziekmakenmetai.nl/mcp",
      "disabled": false
    }
  }
}
```

Authentication: OAuth with PKCE (S256), dynamic client registration and client ID metadata documents, so MCP clients connect without manual setup. Sign in with your muziekmakenmetai.nl account.

With OAuth, Cline opens the sign-in page the first time a tool is used; approve access and return to Cline.

Check the connection by asking: "Make a cheerful Dutch birthday song for my colleague Anna, pop style."
