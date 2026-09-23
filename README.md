# Lightning Leads (Cursor / Grok Bot plugin)

**Connector-only plugin.** This public repo is the installable wrap for Grok Bot and Cursor. It does **not** contain the Lightning Leads mobile apps, backend, or customer data.

Install → sign in with your Lightning Leads account → same paywall / plan / credits as the app. No login = no tools (HTTP 401).

**Publisher:** Lightning Leads  
**License:** MIT (this wrap only)  
**MCP:** https://api.lightningleads.online/marketplace/mcp  
**Server:** `lightning-leads-personal-ai` v1.0.0 (14 tools)

## Install

1. Settings → Plugins → **Lightning Leads** (or load this folder / marketplace listing).
2. Complete Lightning Leads OAuth when prompted.
3. Try: “Give me today’s brief” or “Find leads near 28358 and suggest a route.”

### Manual MCP fallback

- Type: Streamable HTTP
- URL: `https://api.lightningleads.online/marketplace/mcp`
- Name: `lightning-leads`

## What’s public vs private

| Public (this repo) | Private |
| --- | --- |
| `plugin.json` / `mcp.json` | iOS / Android app source |
| Field-sales skills (markdown) | Backend / BBP |
| Logo + MIT license | OAuth secrets, customer data |
| Pointer to hosted MCP URL | Entitlement / billing logic |

## Write safety

Write tools need a stable idempotency key, a server confirmation token, and explicit approval of the exact change. Suggested routes are not saved routes.

## Privacy / support

- https://lightning-leads.com
- https://lightning-leads.com/privacy
- https://lightning-leads.com/terms
- support@lightning-leads.com
