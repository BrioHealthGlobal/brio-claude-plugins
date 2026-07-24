---
name: icp
description: >
  This skill should be used when the user asks to "update Brio's audience
  profile", "who is Brio's ICP", "capture our audience segments", or wants
  to review, refresh, or re-interview for Brio's ideal-customer/audience
  profile. Loads and can update the live shared profile doc.
metadata:
  version: "2.0"
---

# ICP — Audience Capture (Brio Health Global)

Capture or refresh Brio's audience segments — who Brio communicates with,
what those audiences care about, and what language they use.

## Reference doc (live — read fresh every run)

The ICP doc is the shared source of truth in Google Drive, not a bundled
file. See `${CLAUDE_PLUGIN_ROOT}/context-docs/index.md` for the doc ID,
URL, and the full read/propose/write-back process.

Open it via the connected Google Docs/Drive tool first. If the user just
wants to know the existing audiences, answer directly from the doc
without re-running the interview.

## When the user wants to refresh or redo the profile

### Step 1 — Interview
Ask, numbered, all at once:
1. Who are the 1–3 primary audiences Brio communicates with most?
2. For the primary audience: what do they care most about?
3. What problems or frustrations do they bring to Brio?
4. What language do THEY use — specific terms, jargon, phrases?
5. What does a successful interaction with this audience look like?

Wait for the full response before continuing.

### Step 2 — Draft the update
For each segment, write:
- Segment name and one-line description
- Core goals and motivations
- Key frustrations / hesitations / misconceptions
- Language/vocabulary they use
- What they need from Brio's communications
- What turns them off

### Step 3 — Confirm
Show the drafted update next to the current doc content. Ask: "Does this
capture Brio's audiences accurately?" Apply edits based on feedback.

### Step 4 — Write back
Once confirmed, apply the update directly to the live ICP doc (don't just
describe it) and append a dated line to its Change Log section per
`context-docs/index.md` step 4.

## Context drift (outside a full refresh)

If, during any other conversation, the user mentions something that adds
to or contradicts a segment already in the doc, follow the propose →
confirm → write-back flow in `context-docs/index.md` rather than waiting
for a full re-interview.
