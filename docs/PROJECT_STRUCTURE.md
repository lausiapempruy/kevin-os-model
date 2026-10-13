# Project structure

This repository is a growing, provider-agnostic collection of reusable instructions, workflows, and resources for AI models and tools.

## Top-level files

- `README.md` — project overview and starting point.
- `CONTRIBUTING.md` — contribution expectations and review checklist.
- `CODE_OF_CONDUCT.md` — community behavior standards.
- `SECURITY.md` — handling sensitive security reports and secrets.
- `SUPPORT.md` — usage help and issue-reporting guidance.
- `LICENSE` — default license for repository content, subject to file-specific notices.
- `assets/` — project identity artwork.
- `anti-slop-text/` — first reusable writing skill.

## Skill layout

A skill can contain:

- `SKILL.md` — main metadata and workflow instructions.
- `references/` — focused reference material loaded when useful.
- `evals/` — repeatable test cases for checking expected behavior.
- `scripts/` or `assets/` — optional files when a resource genuinely needs them.

Keep each skill focused. Do not add placeholder directories or files just to make a skill look larger.

## Compatibility

The project aims to keep resources readable and usable across models wherever possible. A model that can read Markdown can attempt to follow a skill's instructions, but that does not mean every product supports native skill installation or follows the instructions identically. State what has actually been tested and document known limitations. Never promise universal compatibility without defined and repeatable testing.
