# Brio Brand Skills

A Cowork plugin packaging Brio Health Global's brand voice, audience,
positioning, and visual standards, plus content-production and
evaluation-report workflows — so any teammate can produce on-brand Brio
content or M&E reports.

## Shared source of truth

Unlike a typical plugin, the brand-context material (voice, anti-patterns,
examples, checklist, narrative, ICP, positioning, visual guide, visual
checklist) is **not bundled as static files**. It lives as nine Google
Docs in the **Claude** shared drive, under **Skills → Brio**:
https://drive.google.com/drive/folders/1EgfcXyYSV7yAGLHuVS19tH8c7rj1tjUR

Doc IDs and URLs are listed in `context-docs/index.md`. Every skill reads
these live each time it runs, and — with your confirmation — writes
updates directly back to them when Brio's programs, numbers, or story
change mid-conversation. Because it's one shared doc set (not a copy per
teammate), an approved update is visible to everyone's next session
immediately, with no need to rebuild or redistribute this plugin.

## Components

**Skills:**

| Skill | What it does |
|---|---|
| `brand-voice` | Rewrite or draft any content in Brio's voice; run the brand checklist |
| `icp` | Review, refresh, or live-update Brio's audience segments |
| `positioning` | Review, refresh, or live-update Brio's mission, differentiators, and values |
| `copywriting` | Write or rewrite channel-specific copy (LinkedIn, email, web, donor letters, etc.) |
| `content-pipeline` | Full research → draft → self-review pipeline for a piece of content |
| `visual-brand` | Create or audit visual artifacts (slides, graphics, reports) against Brio's visual standards |
| `eval-report-pipeline` | Full M&E reporting pipeline: intake → data audit → draft → limitations review |
| `report-drafting` | Draft a single evaluation/grant-related report from existing data |

## Setup

**Required:** a Google Docs/Drive connector enabled in this Cowork
workspace, with access to the **Claude** shared drive. Without it, the
brand-context skills can't read or update the live docs and will say so
rather than fabricating content.

No other environment variables or accounts are required. The
`content-pipeline` skill uses a web search tool for its research stage if
one is connected; if not, it drafts from the context docs and your own
input instead.

## Usage

Just describe what you want — e.g. "write a LinkedIn post for Brio about
our new teacher training cohort" or "draft the Q2 program evaluation
report from this survey data." Claude will pick the matching skill
automatically.

## Keeping context current

You don't need to manually edit the Docs or rebuild this plugin for
routine updates (new programs, updated stats, evolving narrative). As
conversations happen:

1. If something a user says conflicts with or extends a context doc, the
   skill quotes the stale/missing part and proposes a specific edit.
2. The user confirms (or edits the proposal) before anything is written.
3. On confirmation, the skill updates the live Google Doc directly and
   logs the change in that doc's Change Log section.
4. Each skill run closes with one catch-all question — "anything about
   Brio's programs, numbers, or story that changed today?" — so updates
   aren't limited to whatever the skill happened to need mid-task.

Full mechanics are in `context-docs/index.md`. Rebuild/redistribute this
plugin only when the *skills themselves* change (new workflow, new
component) — the brand content itself updates live, in place.
