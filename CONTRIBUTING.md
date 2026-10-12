# Contributing

## Adding a new skill

1. Create a folder under `skills/` using kebab-case  
   Example: `skills/code-reviewer/`

2. Add a `SKILL.md` with this structure:

```markdown
---
name: skill-name
description: One clear sentence about what it does and when to use it.
---

# Skill Name

## What it does

## When to activate

## Instructions for the model

(the actual system prompt / rules)
```

3. Optional: add supporting files inside the skill folder (examples, checklists, references).

4. Update the skill table in the root `README.md`.

5. Open a pull request. Describe the skill and why it is useful.

## Rules

- Be specific. Vague “helpful AI” skills will be rejected.
- Prefer short, enforceable rules over long essays.
- If the skill includes visual or design guidance, follow the same anti-slop standards used in this repository.
- Language can be Indonesian or English — stay consistent inside one skill.

That’s all.