# Relevance filter for prompt additions

Use this reference when deciding whether to include a detail that the user did not explicitly say.

## The three-bucket model

### A. Explicit requirements
The user directly stated the detail. Keep it unless it conflicts with a higher-priority safety or feasibility requirement. Do not silently soften or replace it.

### B. Necessary operational details
The detail makes the requested output usable or verifiable and is strongly implied by the task. Add it proportionately.

Examples:
- A multi-page website needs navigation that connects the requested pages.
- Code intended to replace an existing file should identify the target file and return a complete replacement when that is what the user asked for.
- A research summary should distinguish supported findings from uncertainty.
- An image-generation prompt should specify the subject and important composition details already implied by the request.
- A request for a responsive website reasonably includes phone and desktop layout behavior.

### C. Optional enhancements
The detail might be nice but is not required. Do not make it mandatory without user approval. Put it in optional suggestions only if it is clearly useful.

Examples:
- Dark mode for a website when no theme preference was given
- Animations beyond basic interaction feedback
- Export to PDF/CSV when no export is requested
- Accounts, payments, analytics, cloud sync, databases, or admin panels
- Extra sections, pages, or content categories

These are not always bad ideas. They are scope decisions, so do not quietly impose them.

## Relevance test

For each proposed addition, assess:

1. Goal alignment: direct, supportive, weak, or unrelated
2. Scope impact: none, small, moderate, or large
3. Surprise risk: low or high
4. Conflict risk: does it contradict something the user said?
5. Maintenance or cost: does it add a new dependency, service, or ongoing burden?

Include a detail in the main prompt when it is explicit or clearly necessary and proportionate. Otherwise, leave it out or present it as optional. Exclude unrelated or high-surprise ideas entirely.

## Suggestions should be selective

- Default to at most five optional suggestions.
- Do not suggest something already included in the main prompt.
- Do not pad the list to reach five.
- Explain the practical benefit, not just the feature name.
- Avoid making a suggestion if it conflicts with the user's budget, platform, simplicity, privacy, or stated aesthetic.
- If a suggestion would substantially change the project, label it clearly as a scope-expanding option.
- If no suggestion passes the filter, show none.

## Examples

User prompt: “Build a simple personal portfolio website.”

Main prompt can include a responsive layout, sections for the user's projects and contact information, accessible navigation, and instructions not to invent biography details. It should not automatically require a CMS, analytics, login, database, or payment integration.

User prompt: “Make a local-only notes app.”

Keep local storage and the local-only requirement. Do not add cloud sync or user accounts. If backup/export is worth mentioning, offer it as an optional suggestion rather than changing the architecture.

User prompt: “Write a two-paragraph explanation of photosynthesis for a sixth-grade student.”

Keep the two-paragraph limit and age-appropriate explanation. Do not expand it into a lesson plan, quiz, slide deck, or academic paper.

User prompt: “Create a prompt for a cinematic image of a rainy Jakarta street.”

Focus on scene, atmosphere, composition, lighting, and visual style. Do not add website requirements, branding, or an unrelated narrative.
