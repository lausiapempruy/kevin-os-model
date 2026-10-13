# Prompt structure patterns

Use only the sections that materially help the task. A prompt should be complete, not padded.

## General-purpose structure

1. **Outcome:** What should be produced?
2. **Context:** What does the next AI need to know?
3. **Requirements:** What must be present?
4. **Constraints:** What must not happen? Which platform, format, language, or limits apply?
5. **Deliverables:** What exactly should be returned?
6. **Acceptance criteria:** How can completeness and correctness be checked?

For small requests, this can be one compact paragraph. For complex work, use headings and checklists.

## Website or web app

Consider:
- Site purpose and target audience
- Pages and sections actually requested
- Visual direction grounded in user preferences
- Responsive behavior
- Interaction and states
- Technical stack and file boundaries, if known
- Accessibility and semantic HTML where relevant
- Content and asset constraints
- Exact deliverables (complete files, paths, setup steps)
- Acceptance criteria and basic testing

Do not automatically add authentication, a database, a CMS, analytics, subscriptions, payments, admin panels, APIs, or deployment. Include these only when asked or genuinely required.

## Coding and debugging

Consider:
- Language, framework, runtime, version, and environment if known
- Existing code and file paths
- Expected versus actual behavior
- Constraints on dependencies and compatibility
- Reproduction steps and relevant logs
- Requested change and explicit non-goals
- Complete output format and test expectations

Do not invent source code, files, logs, or repository state. If the AI has no access to the user's environment, instruct it to say so rather than claim it ran tests.

## Writing and editing

Consider:
- Purpose, audience, format, length, language, and tone
- Required facts and source material
- Voice to preserve
- Claims to verify and details not to invent
- Structure appropriate to the requested genre
- Whether the output should be a draft, outline, or final copy

Do not force every piece of writing into headings and bullet lists. Keep the requested length and format.

## Research and analysis

Consider:
- Research question and scope
- Time period and geographic scope
- Source quality and citation expectations
- Distinguishing evidence, inference, and uncertainty
- Comparison criteria
- Output format and decision to support

Do not invent citations, statistics, or current facts. If fresh information matters and browsing is unavailable, state the limitation.

## Image-generation prompts

Consider:
- Primary subject and action
- Setting and important objects
- Composition, camera angle, framing, and aspect ratio if relevant
- Lighting, palette, material, and visual style
- Text appearing inside the image, if any
- Elements to include or avoid
- Output purpose

Do not add typography, logos, or text unless wanted or clearly relevant. Avoid conflicting style instructions.

## Planning and strategy

Consider:
- Desired outcome
- Starting situation and known constraints
- Time horizon and available resources
- Priorities and trade-offs
- Concrete steps, checkpoints, and success criteria
- Assumptions and dependencies

Do not present guesses as known facts or inflate a simple plan into an unnecessary management framework.
