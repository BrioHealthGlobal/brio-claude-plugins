---
name: positioning
description: >
  This skill should be used when the user asks about "Brio's positioning",
  "what makes Brio different", "our mission statement", "core values", or
  wants to review, refresh, or re-interview for Brio's positioning —
  mission, differentiators, values, and how Brio reframes common
  misconceptions. Loads and can update the live shared positioning doc.
metadata:
  version: "2.0"
---

# Positioning (Brio Health Global)

Capture or refresh Brio's positioning — mission, differentiators, values,
and how Brio pushes back on common misconceptions.

## Reference doc (live — read fresh every run)

The Positioning doc is the shared source of truth in Google Drive, not a
bundled file. See `${CLAUDE_PLUGIN_ROOT}/context-docs/index.md` for the
doc ID, URL, and the full read/propose/write-back process.

Open it via the connected Google Docs/Drive tool first. If the user just
wants to know Brio's current positioning, answer directly from the doc
without re-running the interview.

## When the user wants to refresh or redo the positioning

### Step 1 — Interview
Ask:
1. In one sentence: what does Brio do and for whom?
2. What makes Brio's approach distinct from others doing similar work?
3. What do you want people to say about Brio after interacting with it?
4. What 3 values are non-negotiable?
5. What's the biggest misconception about Brio's work?

### Step 2 — Draft the update
- One-sentence mission statement
- Differentiators (3–5 bullets)
- Core values with one-line descriptions
- Desired reputation/perception
- Common misconceptions + how Brio reframes them

### Step 3 — Confirm
Show the drafted update next to the current doc content. Ask: "Does this
represent Brio accurately?" Apply edits based on feedback.

### Step 4 — Write back
Once confirmed, apply the update directly to the live Positioning doc
(don't just describe it) and append a dated line to its Change Log
section per `context-docs/index.md` step 4.

## Context drift (outside a full refresh)

If, during any other conversation, the user mentions a new differentiator,
value, or misconception not yet in the doc — or a program/number change
that positioning language depends on — follow the propose → confirm →
write-back flow in `context-docs/index.md` rather than waiting for a full
re-interview.
