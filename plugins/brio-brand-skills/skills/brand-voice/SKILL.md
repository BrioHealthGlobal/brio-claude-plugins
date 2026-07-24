---
name: brand-voice
description: >
  This skill should be used when the user asks to "check the brand voice",
  "rewrite this in Brio's voice", "does this sound like Brio", or wants any
  written content reviewed or rewritten for tone, register, or rhythm.
  Also use proactively when content sounds generic, corporate, AI-written,
  or off-brand for Brio Health Global.
metadata:
  version: "2.0"
  argument-hint: "[content to rewrite, or describe what to write]"
---

# Brand Voice (Brio Health Global)

Apply Brio's brand voice to written content. Use for any copy where tone,
register, or rhythm matters — long-form, short-form, internal, external.

## Reference docs (live — read fresh every run)

Context docs live in Google Drive, not bundled in this plugin. See
`${CLAUDE_PLUGIN_ROOT}/context-docs/index.md` for doc IDs, URLs, and the
full read/propose/write-back process. You need:

- Voice Guide
- Anti-Patterns
- Examples
- Checklist
- Narrative

Open all five via the connected Google Docs/Drive tool before drafting or
reviewing anything. Do not reuse a read from earlier in the conversation
or a prior session — the docs may have changed.

## When invoked

**If no content or topic is given:** ask "What would you like written or
reviewed for Brio?"

**If rewriting existing content:**
1. Apply Brio's voice per the Voice Guide.
2. Return: (1) the revised version, (2) a brief note on the major voice
   edits made, (3) any phrases that still feel off-brand even after the
   rewrite — flag these explicitly rather than silently forcing a fix.
3. Run the result through the Checklist line by line before returning it.

**If writing from scratch:**
1. Draft fully in Brio's voice, applying the structural rules in the
   Voice Guide.
2. Run the draft through the Checklist before returning it.
3. Cross-check every sentence against the banned list in Anti-Patterns.

## Output

Always return the checklist result alongside the draft — which items
passed, and any that required a fix (with the fix noted).

## Context drift

Follow `context-docs/index.md` steps 2–5: if anything the user says
conflicts with or extends the Voice Guide, Anti-Patterns, Examples, or
Narrative, propose the specific edit, get confirmation, then write it
back to the live doc and log it. Before closing, ask the catch-all
question from step 5.
