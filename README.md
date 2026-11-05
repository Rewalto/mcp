# Rewalto MCP server (preview)

Connect an AI agent to Indian commerce data: quick-commerce prices and stock by pin code, marketplace prices and listings.

The server is in **preview**. Tools, inputs and access can change while it is in preview.

- Server address: `https://mcp.rewalto.com/mcp` (streamable HTTP)
- Every tool, what it returns, its inputs and its credit cost: https://rewalto.com/developers/mcp
- Public tool list, free, no key: https://api.rewalto.com/v1/mcp/tools
- Official MCP Registry name: `com.rewalto/mcp`

This repository holds the listing only: this README and `server.json`, a copy of the server's entry in the official MCP Registry. The server itself is hosted by Rewalto; there is nothing to install or run from here.

## Connect

Add the server address to any MCP client that supports remote (streamable HTTP) servers. For example:

```json
{
  "mcpServers": {
    "rewalto": {
      "type": "http",
      "url": "https://mcp.rewalto.com/mcp"
    }
  }
}
```

Claude Code:

```sh
claude mcp add --transport http rewalto https://mcp.rewalto.com/mcp
```

The first time you connect, your client opens **Sign in with Rewalto** in the browser. To use an API key instead, send the header `Authorization: Bearer <your Rewalto API key>`. Create a key after signing in at https://rewalto.com.

## Cost

Catalogue and account tools are free. Data reads use credits only for data actually delivered, and a read that delivers nothing costs nothing. Every account gets free credits each month. Current prices: https://rewalto.com/pricing

## Links

- Website: https://rewalto.com
- Developer docs: https://rewalto.com/developers
