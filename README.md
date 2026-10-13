# Kevin OS Model

An open, growing collection of reusable instructions, workflows, and resources for working with AI models.

The project is designed to be **provider-agnostic**: resources should be useful with any model that can understand the relevant instructions or file format. Actual support depends on the model, product, interface, context limits, and import mechanism. No single repository format can guarantee native installation or identical behavior across every AI product.

## First resource: anti-slop-text

`anti-slop-text` is a portable writing workflow for reducing generic, repetitive, inflated, and formulaic writing while preserving meaning, evidence, and the writer's voice.

- [Open the skill](anti-slop-text/SKILL.md)
- [Patterns reference](anti-slop-text/references/patterns.md)
- [Review checklist](anti-slop-text/references/review-checklist.md)
- [Examples](anti-slop-text/references/examples.md)
- [Evaluation cases](anti-slop-text/evals/evaluation-cases.md)

## Using the resource

The skill uses the open Agent Skills-style `SKILL.md` format. AI tools that support this format can load it as a skill. Other models can use it by receiving the file contents as instructions, if their interface allows that. A folder containing `SKILL.md` is not automatically installable in every chat app.

1. Open the skill folder and read `SKILL.md`.
2. Follow the installation method documented by your chosen AI tool, if it supports skills.
3. If native skill installation is unavailable, provide the instructions as context or adapt them to that product's custom-instructions feature.
4. Test the resource on real examples and report reproducible issues.

## Compatibility and honest claims

This project aims for broad portability, not a universal guarantee. A resource is not described as "working on every AI" unless that claim can be tested meaningfully across a defined set of models and versions. Model outputs vary, and a prompt cannot override a model's system rules or product limitations.

Likewise, anti-slop-text does not promise "100% anti-slop" or guaranteed passage through AI-writing detectors. Text quality is subjective and context-dependent, and detectors can misclassify both human and AI-assisted writing. The skill focuses on editorial quality, specificity, factual accuracy, and preserving the author's real voice.

## Contributing

New resources are welcome. Keep them focused, document prerequisites and limitations, include examples or evaluation cases where useful, and do not claim testing that did not happen. See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

The repository uses the [MIT License](LICENSE) unless a resource includes a more specific notice.
