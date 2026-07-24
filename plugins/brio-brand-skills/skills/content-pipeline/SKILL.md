---
name: content-pipeline
description: >
  This skill should be used when the user wants end-to-end content
  production for Brio in one run — research, draft, self-review, and
  publish-ready output — rather than just a rewrite. Trigger on requests
  like "produce a full LinkedIn post on X from scratch, research included"
  or "run the full content pipeline on this topic".
metadata:
  version: "2.0"
  argument-hint: "[channel] + [topic or seed idea]"
---

# Content Pipeline (Brio Health Global)

End-to-end content production for Brio in one run: research → draft →
self-review → publish-ready output.

## Reference docs (live — read fresh every run)

Context docs live in Google Drive, not bundled in this plugin. See
`${CLAUDE_PLUGIN_ROOT}/context-docs/index.md` for doc IDs, URLs, and the
full read/propose/write-back process. You need: Voice Guide,
Anti-Patterns, Checklist, ICP, Positioning, Narrative.

## Process

### Stage 1 — Brief
If channel or topic is missing, ask ONE question covering both. Wait for
the full response before continuing.

### Stage 2 — Research
If a web search tool is available, find:
- 2–3 relevant data points or recent developments on the topic
- 1 contrarian or complicating angle
- Any partner orgs / referral sources / collaborators relevant to Brio

If no web search tool is available, say so and draft from the context
docs and the user's own input instead. Hold findings internally — do not
output this stage on its own.

### Stage 3 — Draft
Apply all loaded reference docs. Identify which ICP segment this serves.
Apply channel-specific tone guidance and structural rules from the Voice
Guide. Check every sentence against the banned list in Anti-Patterns.

### Stage 4 — Self-review
Work through the Checklist line by line. Fix any failed items directly
and log the change.

### Stage 5 — Return output
1. Final draft (post-checklist)
2. Research sources used (with URLs), if research was run
3. Checklist fixes made (one line each)
4. ICP segment served and why
5. One alternative opening line

### Stage 6 — Save
Ask if the user wants this saved, and where — the user's own project
folder, not the shared context docs. Then ask: "Ready to publish, want
edits, or should I draft a version for a different channel?"

## Context drift

If research or the user's input surfaces something not reflected in
Narrative, ICP, or Positioning (a new program, an updated stat, a new
partner), follow the propose → confirm → write-back flow in
`context-docs/index.md` before Stage 6.
