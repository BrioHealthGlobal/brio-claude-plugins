---
name: copywriting
description: >
  This skill should be used when the user asks to write or rewrite Brio
  copy for any channel — LinkedIn, email, web, print, internal comms,
  donor letter, or speaking bio. Trigger on requests like "write a LinkedIn
  post for Brio about X", "draft a donor letter", or "rewrite this for our
  website".
metadata:
  version: "2.0"
  argument-hint: "[channel] + [topic or content to rewrite]"
  dependencies: "brand-voice"
---

# Copywriting (Brio Health Global)

Write or rewrite original copy for any channel for Brio — LinkedIn, email,
web, print, internal comms, donor letter, speaking bio, referral outreach.

## Reference docs (live — read fresh every run)

Context docs live in Google Drive, not bundled in this plugin. See
`${CLAUDE_PLUGIN_ROOT}/context-docs/index.md` for doc IDs, URLs, and the
full read/propose/write-back process. You need:

- Voice Guide, Anti-Patterns, Checklist
- ICP
- Positioning
- Narrative

Open all six via the connected Google Docs/Drive tool before drafting.

## Process

### Step 1 — Clarify
If channel or topic is missing, ask ONE question covering both:
"What's this for — which channel, and what topic?"

### Step 2 — Load context
Read all reference docs above. Identify which ICP segment this piece
serves. Note any channel-specific tone guidance in the Voice Guide.

### Step 3 — Draft
Write a complete first draft in Brio's voice. Apply the structural rules
from the Voice Guide, and any channel-specific principles it documents.

### Step 4 — Self-review
Run the draft through the Checklist line by line. List any items that
failed and the fix applied. Cross-check against the banned list in
Anti-Patterns.

### Step 5 — Return output
Return:
1. The draft
2. One-line note: which ICP segment this serves and why
3. Any phrases that still feel borderline — flag explicitly
4. Optional: one alternative version of the opening line

### Step 6 — Save
Ask if the user wants this saved, and where — the user's own project
folder, not the shared context docs.

## Context drift

While drafting, if the topic surfaces a new program, updated statistic,
or story detail not reflected in Narrative, ICP, or Positioning, follow
the propose → confirm → write-back flow in `context-docs/index.md`
before finishing. Ask the catch-all question from step 5 before closing.
