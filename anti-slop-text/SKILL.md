---
name: anti-slop-text
description: Improve drafts and newly written text by removing generic, repetitive, inflated, formulaic, and context-free AI-sounding writing while preserving meaning, evidence, the author's voice, and the intended audience. Use for drafting, rewriting, editing, reviewing, or diagnosing text in any language. Do not use as a promise to bypass AI detectors or to disguise authorship.
license: MIT
metadata:
  author: Kevin
  version: "1.0.0"
---

# anti-slop-text

## Purpose

Write text that feels specific, natural, credible, and fit for its actual purpose. Remove avoidable writing habits commonly associated with low-quality AI output ("AI slop") without making the result artificially casual, imperfect, or theatrical.

This skill is model-agnostic at the instruction level: any model that can read and follow Markdown instructions can attempt to apply it. That does **not** mean every product supports native skill installation, follows every instruction, or produces identical results. Treat this as a portable writing workflow, not a guarantee.

## Core operating rules

1. **Understand the job before editing.** Identify the text type, audience, purpose, language, requested tone, length, and any facts or phrases that must remain. If the context is already clear, do not ask unnecessary questions.
2. **Preserve the author's meaning.** Do not invent experience, sources, data, quotes, credentials, events, or personal opinions. Do not change a cautious claim into a certain one.
3. **Prefer concrete meaning over surface style.** Replace vague praise, broad claims, and empty transitions with details that are supported by the source material. If no details are available, narrow the claim or ask for the missing information instead of fabricating it.
4. **Keep a believable voice.** Match the user's existing register, dialect, language, and level of formality. Do not force slang, typos, jokes, contractions, or first-person anecdotes to make text seem human.
5. **Use the simplest structure that fits.** Headings, bullets, tables, and summaries are tools, not requirements. Use them only when they improve navigation or comprehension.
6. **Vary rhythm for a reason.** Mix sentence lengths naturally. Avoid both monotonous sentence patterns and random variation added as decoration.
7. **Be concise, not skeletal.** Remove repetition and padding, but retain explanations, qualifications, examples, and context that the reader actually needs.
8. **Keep uncertainty honest.** Mark estimates, interpretations, disputed claims, and missing evidence. Never imply that research or verification happened when it did not.
9. **Respect the source and the assignment.** Preserve required terminology, citations, quotations, formatting, accessibility, and legal or technical precision. Do not paraphrase quotations as if they were the original.
10. **Do not optimize for detector scores.** AI-writing detectors can be wrong and their results are not a reliable measure of authorship. Do not promise a detector result or rewrite with the goal of fooling a detector. Improve the text on ordinary editorial merits: clarity, specificity, originality of thought, evidence, and the author's genuine voice.

## Workflow

### Step 1 — Diagnose the draft or brief

For existing text, scan for:
- Repeated points stated in different words.
- Generic claims that could describe almost any topic.
- Introductions that announce importance without saying anything useful.
- Conclusions that merely repeat the opening.
- Overused transitions and signposting.
- Excessive headings, bullet lists, bold text, or symmetrical paragraph structures.
- Inflated adjectives, promotional tone, and unsupported superlatives.
- Repeated sentence openings, identical sentence lengths, or mechanically balanced clauses.
- Abstract nouns where a direct verb would be clearer.
- Formulaic contrasts such as "not just X, but Y" when the contrast adds no real information.
- Stock phrases, canned empathy, empty "in today's world" openings, and generic calls to action.
- Unnecessary em dashes, parenthetical asides, or repeated three-item lists.
- A polished tone that conflicts with the user's intended voice.
- Citations, facts, and examples that look unsupported or do not match the claim.

These are warning signs, not a blacklist. A phrase is not bad simply because an AI sometimes uses it. Keep it when it is the clearest and most accurate choice.

For a new draft, infer the same risks from the prompt and plan the text around the actual subject, not a generic template.

### Step 2 — Establish what must not change

Record mentally or explicitly:
- Main point and intended outcome.
- Facts, names, dates, figures, terminology, and citations.
- Required length or format.
- Intended audience and level of knowledge.
- Voice cues from the user's own writing.
- Any required wording or constraints.

If source material is incomplete, do not fill gaps with invented specificity.

### Step 3 — Edit at the right level

Use this order:
1. **Substance:** Is the point meaningful, accurate, and supported?
2. **Structure:** Does the order help the reader understand it?
3. **Specificity:** Are claims connected to concrete facts, examples, mechanisms, or implications?
4. **Voice:** Does it sound appropriate for this writer and audience?
5. **Sentence craft:** Remove repetition, stale phrasing, awkward rhythm, and needless complexity.
6. **Proofreading:** Check grammar, spelling, punctuation, names, numbers, citations, and consistency.

Do not start by swapping words for synonyms. Sentence-level polishing cannot rescue a vague or unsupported argument.

### Step 4 — Make targeted changes

Prefer:
- Naming the actual subject instead of saying "this aspect" or "various factors."
- Explaining the mechanism or consequence instead of saying something is "important."
- Using active verbs when the actor is known and relevant.
- Giving one useful example instead of several generic ones.
- Keeping a small amount of natural repetition when it aids comprehension.
- Using direct openings that begin with the topic, question, event, or conclusion.
- Ending when the job is done rather than adding a ceremonial summary.
- Keeping a human author's distinctive wording when it is clear and appropriate.

Avoid:
- Inventing personal details to create authenticity.
- Adding deliberate mistakes, fake hesitation, or random slang.
- Replacing every common phrase with an unusual synonym.
- Flattening technical, academic, legal, or safety-critical language just to make it casual.
- Deleting necessary nuance solely to make the text shorter.
- Rewriting a user's whole piece when a light edit would solve the problem.

### Step 5 — Match the requested level of intervention

- **Proofread:** Correct errors only; preserve wording and structure wherever possible.
- **Light edit:** Fix awkward phrasing and obvious repetition while keeping the draft recognizably the same.
- **Rewrite:** Rebuild sentences and structure while preserving the author's meaning and constraints.
- **Create from brief:** Draft from the supplied facts and purpose; ask only for information that is essential.
- **Audit:** Identify the specific weak passages, explain why they underperform, and offer targeted replacements.
- **Critique:** Give a grounded assessment, not a fake numerical "AI score" or a guarantee about detector outcomes.

If the user does not specify, choose the least invasive level that achieves the goal.

### Step 6 — Final quality check

Before returning the text, check:
- Does every paragraph do a clear job?
- Could any sentence be removed without losing meaning?
- Are important claims specific enough and supported?
- Did the edit preserve the original meaning, language, and requested tone?
- Did any new fact, quote, source, or personal experience slip in?
- Are transitions and headings actually useful?
- Does the ending add something, or can the text simply stop?
- Does the result still sound appropriate for the context rather than generically "humanized"?
- Are all constraints met?

If the user asks for an audit, briefly report the most important edits. If they ask only for a finished draft, return the draft without a long lecture.

## Output behavior

- For a direct rewrite request, prioritize the revised text.
- For an audit request, cite the exact phrase or passage being discussed and provide a concrete alternative.
- For a new draft, do not narrate the whole writing process unless asked.
- Do not automatically append "In conclusion," a summary, a list of changes, or a follow-up offer.
- If the text is already strong, say so briefly and change only what genuinely needs changing.
- Keep the language of the response aligned with the user's language unless they request otherwise.

## References

Load `references/patterns.md` when diagnosing recurring AI-slop patterns in detail.
Load `references/review-checklist.md` when conducting a systematic text audit.
Load `references/examples.md` for illustrative before/after edits and why they work.
