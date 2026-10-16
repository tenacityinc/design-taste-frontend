# design-taste-frontend

Anti-slop frontend design for landing pages, portfolios, and redesigns. The agent reads the brief, infers the right design direction, and ships interfaces that do not look templated. Works in Cursor and Claude Code. Not intended for dashboards, data tables, or multi-step product UI.

## Use

### Cursor

1. Open **Customize** in the sidebar.
2. Install **design-taste-frontend** at **Project** scope from `https://github.com/tenacityinc/design-taste-frontend`. Accept the marketplace trust prompt if shown.
3. Run **Developer: Reload Window**.
4. In Agent chat, type `/design-taste` and select it from the slash palette.

If Customize does not list it, paste the GitHub URL into plugin search, install at Project scope, then reload.

When this repository is the workspace, `/design-taste` is also available from `.cursor/commands/design-taste.md` after a reload.

### Claude Code

```
/plugin marketplace add tenacityinc/design-taste-frontend
/plugin install design-taste-frontend@design-taste-frontend
/reload-plugins
```

Then type `/design-taste` in chat, or invoke the `design-taste-frontend` skill with the Skill tool. The skill also activates on landing-page, portfolio, and redesign work.

### What to say after the slash

Give a short brief: page kind, audience, and vibe.

Example: `/design-taste SaaS landing for technical buyers, Linear-clean`

### Out of scope

Do not use this for dashboards, data tables, or Electron product UI (including HCB Desktop caption chrome).

## What's inside

- `plugins/design-taste-frontend/skills/design-taste-frontend/SKILL.md` -- the core skill (upstream tasteskill v2, with our scope guard): the run, the house rules and the laws of the craft. It loads `references/*.md` (copy, type, colour, layout, imagery, motion, critique, tells, research) on demand.
- `.cursor/commands/design-taste.md` and `plugins/design-taste-frontend/commands/design-taste.md` -- the `/design-taste` slash command (same command, two discovery paths: this repo vs plugin install).
- `.cursor-plugin/marketplace.json` -- Cursor marketplace manifest for Customize -> Project install.
- `.claude-plugin/marketplace.json` -- Claude Code marketplace manifest.

## Updating

Bump `version` in:

- `.claude-plugin/marketplace.json`
- `plugins/design-taste-frontend/.claude-plugin/plugin.json`
- `.cursor-plugin/marketplace.json`
- `plugins/design-taste-frontend/.cursor-plugin/plugin.json`

Then push to `main`. Claude Code consumers run `/plugin update design-taste-frontend@design-taste-frontend` (or `/reload-plugins`). Cursor consumers reload the window after the plugin updates.

## Evals

Five cases live in `plugins/design-taste-frontend/evals/` (the default eval directory for `claude plugin eval`). Four are positive design cases ported from upstream (`saas-invoicing`, `restaurant-osteria`, `portfolio-designer`, `product-ceramics`), each graded by an LLM on the house rules and on whether the idea comes from the subject. One is a negative case (`out-of-scope-caption-dashboard`): an HCB Desktop caption overlay plus a data dashboard, where the skill must decline to apply landing-page styling. Cases use only Read, Glob, Grep and Skill; there are no scaffold scripts, MCP servers or Bash.

Running them calls the model on your account and costs money, so set a ceiling:

```
claude plugin eval plugins/design-taste-frontend --max-cost-usd 2
```

Add `--runs 1` for a cheaper smoke run, or `--case 'out-of-scope*'` to run one case.

## Credits

Based on [Leonxlnx/taste-skill](https://github.com/Leonxlnx/taste-skill) (MIT, copyright (c) 2026 Leonxlnx). Modified by Tenacity. See [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md) for the full license text and the commit this was copied from.
