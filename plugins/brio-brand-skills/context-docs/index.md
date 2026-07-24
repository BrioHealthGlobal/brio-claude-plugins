# Brio context docs — live source of truth

These are Google Docs in the **Claude** shared drive, under
**Skills → Brio**. They are the *only* copy — this plugin does not bundle
local snapshots, so every skill run reads the current version and any
approved edit updates it for the whole team immediately.

Folder: https://drive.google.com/drive/folders/1EgfcXyYSV7yAGLHuVS19tH8c7rj1tjUR

| Doc | Doc ID | URL |
|---|---|---|
| Voice Guide | `1q9bK_gSocGgHdWQMrtXCP6Sq4naZamvFltYI7c2xOOY` | https://docs.google.com/document/d/1q9bK_gSocGgHdWQMrtXCP6Sq4naZamvFltYI7c2xOOY/edit |
| Anti-Patterns | `1Po-cax7FlLCLfx5wDIj2Rd4E15lrIGvyZIvIyJNAbkI` | https://docs.google.com/document/d/1Po-cax7FlLCLfx5wDIj2Rd4E15lrIGvyZIvIyJNAbkI/edit |
| Examples | `1moVqNdYksCyWO3YiM2C8tjLndqLd-V77u8o6-AqCDDo` | https://docs.google.com/document/d/1moVqNdYksCyWO3YiM2C8tjLndqLd-V77u8o6-AqCDDo/edit |
| Checklist | `1ZIEfRDDFe3JajLZtekSPeQ_WlFi869MfTGGdwPwMtPk` | https://docs.google.com/document/d/1ZIEfRDDFe3JajLZtekSPeQ_WlFi869MfTGGdwPwMtPk/edit |
| Narrative | `1BNd-I6hXODesJOVk0Qaqzj99F68Mc8H0tWITGcvRQmE` | https://docs.google.com/document/d/1BNd-I6hXODesJOVk0Qaqzj99F68Mc8H0tWITGcvRQmE/edit |
| ICP | `11Pvj3dpmzbwfKj6sMwpkxSCklALInIAeTrgA9HEV0uE` | https://docs.google.com/document/d/11Pvj3dpmzbwfKj6sMwpkxSCklALInIAeTrgA9HEV0uE/edit |
| Positioning | `1TWIsGWjUB0Ir5gAunJLZKllKoZVI3eMjelKMZ0BoNk4` | https://docs.google.com/document/d/1TWIsGWjUB0Ir5gAunJLZKllKoZVI3eMjelKMZ0BoNk4/edit |
| Visual Guide | `13x3-cPFeV3sb8d8SPGJllnmEgEb8dJsB9td9yno4NfQ` | https://docs.google.com/document/d/13x3-cPFeV3sb8d8SPGJllnmEgEb8dJsB9td9yno4NfQ/edit |
| Visual Checklist | `1939Xegax_p8A5nUNaiLQwexG_nir58GN_ORo-dptVGo` | https://docs.google.com/document/d/1939Xegax_p8A5nUNaiLQwexG_nir58GN_ORo-dptVGo/edit |

## How skills use these

1. **Read fresh every run** — open the doc via whatever Google Docs/Drive
   tool is connected in this session (MCP connector, or the `gws` CLI if
   available). Never rely on a cached read from earlier in the
   conversation or a prior session.
2. **Watch for drift while working** — if the user mentions a new
   program, an updated statistic, a changed partner, or anything that
   contradicts or extends what's in a doc, don't silently use the old
   version and don't silently rewrite the doc either.
3. **Propose, don't auto-apply** — quote the stale/missing line, propose
   the specific replacement text, and ask the user to confirm before
   writing anything back.
4. **On confirmation, write it back to the live doc** — apply the edit
   directly to the Google Doc (so every teammate's next session sees it),
   and append a dated line to that doc's "Change Log" section (create one
   at the bottom if it doesn't exist yet):
   `[YYYY-MM-DD] — [what changed] — confirmed by [user]`
5. **Close with one catch-all question** — before ending a skill's main
   output, ask: "Anything about Brio's programs, numbers, or story that
   changed today that these docs should reflect?" Treat any answer the
   same way as step 3–4.

If no Google Docs/Drive tool is connected in this session, say so
explicitly and fall back to answering from what's pasted in the
conversation — do not fabricate doc contents.
