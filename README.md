# Reverse email lookup by Senderscope

Reverse email lookup, email finder and email verifier for B2B in your AI assistant. This MCP server connects Senderscope to Claude and other MCP clients: ask who owns this email and get the professional profile behind a work address, find a work email from a name and company domain, and run email verification before you send.

get_account reads your plan and credits. lookup_email returns the professional profile and deliverability behind a work email; find_email finds a work email from a name and company domain or a LinkedIn URL; verify_email checks deliverability, accept-all, SPF and DMARC. Each uses one credit only when it returns a result. list_lookups and get_lookup read your history for free.

## Remote MCP

Use **https://senderscope.app/mcp** in a client that supports remote MCP with OAuth. Sign in to Senderscope and approve the connection. Clients without OAuth can send a Senderscope API key as `Authorization: Bearer ssk_live_…`.

## Claude Desktop and other stdio clients

Requires Node.js 22 or newer. Add this configuration:

```json
{
  "mcpServers": {
    "senderscope": {
      "command": "npx",
      "args": ["-y", "senderscope-mcp"]
    }
  }
}
```

Or install the `.mcpb` file from [Releases](https://github.com/senderscope/mcp-server/releases) in your desktop client's Extensions settings. The connector opens your browser for sign-in.

Professional data only. Not for FCRA purposes. People can opt out at https://senderscope.app/opt-out/.

[Website](https://senderscope.app) · [MCP & API](https://senderscope.app/mcp-api/) · [Privacy](https://senderscope.app/privacy/)
