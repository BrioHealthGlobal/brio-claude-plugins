# brio-claude-plugins

Internal Claude plugin marketplace for Brio Health Global.

## Add this marketplace

```
/plugin marketplace add airos21/brio-claude-plugins
```

## Install the plugin

```
/plugin install brio-brand-skills@brio-tools
```

## Requirements

You need a Google Docs/Drive connector enabled and access to the
**Claude** shared drive (Skills → Brio) for the brand-context skills to
work — see `plugins/brio-brand-skills/README.md` for details.

## Updating

Whoever maintains this repo bumps `version` in
`plugins/brio-brand-skills/.claude-plugin/plugin.json` and pushes.
Teammates get the update by running `/plugin marketplace update` (or it
refreshes automatically in the background).
