---
name: design-taste
description: Invoke design-taste-frontend (tasteskill) for landing pages, portfolios, and redesigns. Not dashboards or product UI.
---

# /design-taste

Invoke the **design-taste-frontend** skill (internally called tasteskill). Do not invent a second workflow.

## When to use

Use this for landing pages, portfolios, and marketing or editorial redesigns.

Do not use this for dashboards, data tables, multi-step product UI, or Electron product UI such as HCB Desktop caption chrome.

## What to do

1. Read the skill file and follow it. Do not paste the skill into the conversation and do not rewrite it from memory.
   - If this repository is the workspace, read `plugins/design-taste-frontend/skills/design-taste-frontend/SKILL.md`.
   - If the plugin is installed in another project, read the installed skill `design-taste-frontend` (`skills/design-taste-frontend/SKILL.md` from the plugin root).
2. Treat any text after `/design-taste` as the brief. Infer page kind, audience, and vibe.
3. State a one-line design read, then ship using only the rules that fit the brief.
