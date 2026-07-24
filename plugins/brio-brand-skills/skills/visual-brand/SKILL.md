---
name: visual-brand
description: >
  Use when reviewing or producing a visual artifact for Brio Health Global —
  slides, graphics, layouts, designed reports, or any output where color,
  type, or logo choices are being made. Do not use for copy-only requests;
  use the copywriting skill instead.
metadata:
  version: "2.0"
---

# Visual Brand (Brio Health Global)

Visual consistency protects brand trust and signals credibility. Every
visual artifact must conform to Brio's brand standards before it ships.

## Reference docs (live — read fresh every run)

Context docs live in Google Drive, not bundled in this plugin. See
`${CLAUDE_PLUGIN_ROOT}/context-docs/index.md` for doc IDs, URLs, and the
full read/propose/write-back process. You need:

- Visual Guide — authoritative color palette, typography rules, and logo
  usage standards. Read this in full; do not rely on recalled values from
  a prior turn.
- Visual Checklist

## Process

### Step 1 — Clarify the artifact
If not already clear, confirm:
- What is being created or reviewed (slides, graphic, report layout, etc.)
- Net-new creation or review of existing work
- Whether logo placement is required

Do not proceed until the artifact type is confirmed.

### Step 2 — Apply or audit brand standards

**If creating:** apply all color, typography, and logo rules from the
Visual Guide as you build. Call out every decision and which rule it
follows.

**If reviewing:** audit the artifact against every rule in the Visual
Guide. For each violation found:
- Quote or describe the specific element
- Name the exact rule it breaks
- State the required correction

If no violations, confirm each rule category passed explicitly.

### Step 3 — Run the visual checklist
Work through the Visual Checklist line by line. Do not return a passing
verdict until every item is checked. If any item fails, return to Step 2.

### Step 4 — Output
Return the completed review or created artifact spec, including:
- Artifact type
- Any violations found and corrections applied
- Checklist pass confirmation

Ask if the user wants this saved, and where.

## Context drift

If the artifact reveals a genuinely new visual need not covered by the
Visual Guide (a new logo lockup, a new color use case), follow the
propose → confirm → write-back flow in `context-docs/index.md` rather
than quietly improvising a standard.
