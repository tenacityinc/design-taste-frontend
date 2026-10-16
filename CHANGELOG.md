# Changelog

## 0.3.1

- Eval suite is cheaper and clearer: one run per case, and each positive case replaces the bundled `house-rules` grader with single-rule graders so a failure names the rule.

## 0.3.0

- Moved to the upstream tasteskill v2 core `SKILL.md` plus nine `references/` files loaded on demand (copied from Leonxlnx/taste-skill at commit f624f37, MIT). Upstream scripts, library and assets are not shipped; the skill text was edited to use manual checks instead.
- Kept our scope guard: landing pages, portfolios, marketing and editorial pages, redesigns. Not dashboards, data tables, product UI or HCB Desktop caption UI.
- Dropped the v1-era GSAP sticky-stack and horizontal-pan snippets and the React/Motion stack defaults; v2 is stack-agnostic and covers motion in `references/motion.md`.
- Added credit to the upstream project (`THIRD_PARTY_NOTICES.md`, README Credits).
- Added an eval suite under `plugins/design-taste-frontend/evals/` (see README, Evals).

## 0.2.0

- Added the `/design-taste` slash command for Cursor and Claude Code. Skill based on the upstream experimental v2 skill, with local edits.
