---
name: ll-mcp-setup
description: Install or troubleshoot the Lightning Leads Grok Bot / Cursor plugin and marketplace MCP connector. Use when tools are missing, OAuth fails, or the user asks how to connect Lightning Leads to chat.
---

# Lightning Leads plugin setup

## Install (Grok Bot / Cursor)
1. Settings → Plugins → find **Lightning Leads** (or load this plugin folder).
2. Install / enable.
3. Complete Lightning Leads OAuth when prompted.
4. Confirm tools from server `lightning-leads-personal-ai` (14 tools).

## Manual MCP fallback
- Type: Streamable HTTP
- URL: `https://api.lightningleads.online/marketplace/mcp`
- Name: `lightning-leads`

## Troubleshoot
- No tools: re-auth OAuth; confirm network to `api.lightningleads.online`.
- Writes blocked: run the confirmation protocol in `disposition-and-notes`.
- Support: support@lightning-leads.com
