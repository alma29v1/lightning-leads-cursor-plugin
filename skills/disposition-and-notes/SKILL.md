---
name: disposition-and-notes
description: Log Lightning Leads notes, follow-ups, and dispositions with explicit confirmation. Use when the user wants to mark NI/sale/callback, add a note, or flag a follow-up after a door.
---

# Dispositions and notes

## When to use
- Add a note on a lead
- Set disposition (sale, NI, callback, etc.)
- Mark for follow-up
- Add a custom / manual lead

## Write tools
`add_lead_note`, `set_lead_disposition`, `mark_lead_for_follow_up`, `add_custom_lead`

## Confirmation protocol (required)
1. First call with a stable `idempotencyKey` — do not treat any boolean alone as approval.
2. Show the user the **exact** change the server proposed.
3. Only after clear host/user approval, repeat with `userConfirmation=true` and the server `confirmationToken`.
4. Success only if `status=success`, `verified=true`, and `stateChanged=true`. Duplicates mean no new change.

## Rules
- Never write from inferred consent.
- Never reveal connector tokens.
- `mark_lead_for_follow_up` is destructive-flagged — be extra explicit.
