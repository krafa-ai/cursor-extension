# Krafa

An [Agent Plugins](https://agent-plugins.org) package that points Cursor (and any other conformant client) at `https://app.krafa.ai/api/mcp`. Auth is OAuth on first use. There is no token in this repo.

Call `design_taste` before building or restyling UI so the work matches this account's taste.

## Install

Once this is listed on the [Cursor Marketplace](https://cursor.com/marketplace), install it from Customize. Until then:

1. Symlink this folder into Cursor's local plugin dir:

   ```bash
   ln -s "$(pwd)" ~/.cursor/plugins/local/krafa
   ```

2. Reload the window (**Developer: Reload Window**).
3. Sign in when Cursor prompts for the MCP server.

Or run `npx krafa connect` from the Krafa app.

## Layout

```text
krafa-extension/
├── plugin.json                          # Agent Plugins manifest
├── mcp.json                             # Streamable HTTP MCP server
├── skills/krafa-design-taste/SKILL.md   # Call design_taste before building UI
└── assets/logo.png
```
