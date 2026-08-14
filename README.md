![krafa](https://krafa.ai/og.png)

<p align="center">
  <a href="https://krafa.ai/">
    <h2 align="center">krafa</h2>
  </a>
</p>

<p align="center">Your design taste, as an MCP tool any agent can call before it builds.</p>

### About

This is the [Agent Plugins](https://agent-plugins.org) package for Krafa. It points Cursor (and any other conformant client) at `https://app.krafa.ai/api/mcp`. Auth is OAuth on first use. There is no token in this repo.

Call `design_taste` before building or restyling UI so the work matches this account's taste. The payload is the whole standard; read the routing at the top, then the matching sections.

### Layout

- **plugin.json**: Agent Plugins manifest
- **mcp.json**: streamable HTTP MCP server
- **skills/krafa-design-taste**: tells the agent to call `design_taste` first
- **assets/logo.png**: marketplace mark

### Features

- **One tool**: `design_taste` returns the whole Krafa standard
- **OAuth, no secrets**: sign in on first use
- **Open standard**: root `plugin.json`, not a Cursor-only layout
- **Portable**: any Agent Plugins client can load it

### Install

Once this is listed on the [Cursor Marketplace](https://cursor.com/marketplace), install it from Customize.

Until then, load it locally:

```bash
git clone https://github.com/krafa-ai/cursor-extension
cd cursor-extension
ln -sfn "$(pwd)" ~/.cursor/plugins/local/krafa
```

Reload the window (**Developer: Reload Window**), then sign in when Cursor prompts for the MCP server.

Or run `npx krafa connect` from the Krafa app.

### Development

```bash
git clone https://github.com/krafa-ai/cursor-extension
cd cursor-extension
ln -sfn "$(pwd)" ~/.cursor/plugins/local/krafa
```

Reload Cursor and confirm **krafa** appears under Customize → Plugins. The MCP server is `https://app.krafa.ai/api/mcp`.

***

Built by [Harsh Singh](https://harshsingh.me)
