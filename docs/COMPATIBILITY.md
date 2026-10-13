# Compatibility guide

Kevin OS Model is designed for portability, not magical universal installation.

## Three different kinds of compatibility

| Level | What it means | What we can honestly claim |
|---|---|---|
| Readable | A model or tool can receive the Markdown text. | Plain Markdown is broadly readable, but context limits and interfaces differ. |
| Instruction-following | A model attempts to follow the workflow. | Results vary by model, system instructions, context, and user request. |
| Native integration | A product installs or invokes a resource as a built-in skill. | Only claim this for products and versions where it has actually been verified. |

A skill folder containing `SKILL.md` does not, by itself, make the skill installable in every AI application.

## How to report compatibility

When testing a resource, record:

- Product and model name as displayed by the provider
- Version or release identifier, when available
- Date tested
- How the skill was supplied (native installation, uploaded file, pasted instructions, or another method)
- Task and input used
- Expected behavior and observed behavior
- Known limitations and whether the result was repeatable

Do not infer support for an entire provider from a single model, or support for all versions from one successful test.

## Practical fallback

If native skill installation is unavailable, provide the contents of `SKILL.md` as context or adapt the workflow to the product's custom-instructions feature. Keep the original file as the source of truth so adaptations do not drift.

## Claims we avoid

- “Works perfectly on every AI.”
- “Guaranteed 100% results.”
- “Undetectable by AI detectors.”
- “Overrides the model's safety rules or system instructions.”

Use narrower, testable statements instead. For example: “The Markdown workflow was tested with [model/version] on [date] using [method] and passed [specific evaluation cases].”
