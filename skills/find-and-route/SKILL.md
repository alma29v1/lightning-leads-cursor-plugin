---
name: find-and-route
description: Search Lightning Leads inventory and suggest an efficient knock order. Use when the user wants leads nearby, a street list, a route, or "who should I hit next".
---

# Find leads and route

## When to use
- Find / search leads in an area or by filters
- Build or reorder a knock list
- "Who’s next on my route?"

## Steps
1. Clarify area or filters if missing (city, ZIP, campaign, status).
2. Call `find_leads` and/or `search` / `fetch` as appropriate.
3. For knock order, call `get_route_planning_context` then `suggest_route_order`.
4. Present a short ordered list with address + reason. Say clearly that a suggested order is **not** a saved route.

## Rules
- `find_leads` and `suggest_route_order` never persist state.
- Do not claim a route was saved.
