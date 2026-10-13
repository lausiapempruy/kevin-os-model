---
name: prompt-upgrade
description: Turn a user's rough prompt into a detailed, ready-to-use prompt for almost any task, including websites, coding, research, writing, design, analysis, and planning. Preserve the user's actual intent, infer only safe and necessary defaults, filter optional enhancements for relevance, and provide a small set of clearly separated suggestions. Use when the user asks to improve, expand, optimize, or make a prompt more complete. Do not execute the prompt unless the user also asks for the task itself.
license: MIT
metadata:
  author: Kevin
  version: "1.0.0"
---

# prompt-upgrade

## Purpose

Transform a short, vague, messy, or incomplete user prompt into a clear, detailed, actionable prompt that is more likely to produce a strong result in one pass.

The goal is to reduce avoidable back-and-forth by making the prompt explicit about the user's intended outcome, requirements, constraints, deliverables, and acceptance criteria. The skill can be used for many task types and AI products; the prompt should not assume a specific provider unless the user names one.

This skill improves the request. It does not guarantee perfect output, eliminate all follow-up questions, reduce token usage in every case, or bypass any provider's usage limits. A detailed prompt can sometimes be longer than the original, but it may reduce repeated revisions.

## Core rule: preserve the user's intent

Treat the user's original prompt as the source of truth.

- Keep the same main goal, subject, audience, language, platform, style, and constraints.
- Do not silently change the task, invent a business goal, add features, or expand the scope just because an idea seems impressive.
- Do not treat "make it the best" as permission to add every feature imaginable.
- Make the prompt complete in the dimensions that matter to the stated goal, not bloated.
- Never claim that the user requested a detail they did not request.
- If an assumption is useful but not certain, either state it explicitly as an assumption inside the prompt or leave it out.
- If a missing detail is truly blocking, ask one concise clarification instead of guessing. Otherwise proceed with reasonable, low-risk defaults and label important assumptions.

## When to use

Use this skill when the user gives a prompt and wants it improved, expanded, clarified, optimized, made more professional, made more detailed, or prepared for another AI to execute.

It applies to prompts for, among other things:
- Websites, web apps, UI/UX, HTML/CSS/JavaScript, and product prototypes
- Software engineering, debugging, scripts, and automation
- Writing, editing, reports, presentations, and educational materials
- Research, comparison, planning, and analysis
- Visual design, image generation, branding, and creative work
- Business workflows, documentation, and structured deliverables

Do not assume these categories require the same structure. Use a format that fits the task.

## Workflow

### 1. Extract the intent

Internally identify:
- **Goal:** What should the next AI produce or accomplish?
- **Subject and context:** What is being made, changed, studied, or solved?
- **Audience and use:** Who is it for and where will it be used, if stated?
- **Must-haves:** Explicit requirements that must survive the rewrite.
- **Constraints:** Platform, language, style, budget, deadline, files, technical limits, safety, and exclusions.
- **Deliverable:** What exactly should the AI return?
- **Acceptance criteria:** What would make the result complete and usable?
- **Unknowns:** Which details can be reasonably defaulted and which are genuinely blocking?

Do not display a long analysis unless the user asks for it. Use this extraction to write a better prompt.

### 2. Separate requirements from enhancements

Classify details into three buckets:

1. **Explicit requirements:** Directly stated by the user. Preserve them.
2. **Necessary operational details:** Details needed to make the request executable, such as asking for complete files when the user wants ready-to-use code, specifying mobile responsiveness for a website intended for multiple screen sizes, or requiring the AI to state assumptions and avoid invented facts.
3. **Optional enhancements:** Ideas that could be useful but are not necessary to fulfill the request.

Explicit requirements always take priority. Necessary operational details may be added when they directly support the goal and do not change the scope. Optional enhancements must be filtered by relevance and must not be silently inserted as mandatory features.

### 3. Apply the relevance filter to every addition

Before adding a detail, ask:
- Does it directly help achieve the user's stated goal?
- Is it implied by the requested deliverable or necessary for it to work?
- Does it conflict with any explicit requirement, preferred style, platform, or simplicity constraint?
- Does it create significant extra implementation, cost, maintenance, dependencies, privacy exposure, or complexity?
- Would a reasonable user be surprised to find it in the prompt?

If an addition is unrelated, speculative, scope-expanding, or likely to surprise the user, remove it. If it is potentially valuable but not clearly implied, put it under a separate **Optional suggestions** section rather than inside the main prompt. Do not list suggestions that fail the same relevance test.

Examples:
- A request for a simple static landing page does not automatically need authentication, a database, a payment system, analytics, a CMS, or an admin dashboard.
- A request for a dashboard does not automatically mean it needs live APIs, user accounts, role-based access, charts of invented data, or cloud deployment.
- A request for a website does commonly benefit from responsive layout, accessible controls, coherent navigation, and basic error handling, but the prompt should scale these requirements to the actual project.
- A request for an image prompt does not need coding architecture, web accessibility, or deployment steps.
- A request for a short school explanation should not be turned into a research paper unless requested.

### 4. Build the upgraded prompt

Choose a structure suitable for the task. When useful, include:
- Role or expertise, only if it meaningfully helps
- Context and intended outcome
- Exact task
- Functional and content requirements
- Visual, tone, or stylistic direction
- Technical environment and constraints
- Required inputs and how to handle missing information
- Deliverables and output format
- Quality checks and acceptance criteria
- A short instruction to avoid unrequested features, fabricated facts, placeholders, and incomplete deliverables

Be concrete. Replace vague language like "make it the best" with criteria grounded in the user's request. Do not invent factual content to make a prompt appear complete.

### 5. Prevent avoidable rework

When appropriate to the task, tell the next AI to:
- Review all explicit requirements before starting.
- Identify genuine blockers; do not ask questions whose answers can be safely inferred.
- State any important assumptions briefly before acting, or use sensible defaults if the user wants direct execution.
- Plan the implementation before making changes when the task is complex.
- Produce the requested deliverable in full, not just a vague outline, mock response, or disconnected fragments.
- Check the result against each requirement before finalizing.
- Fix discovered issues before presenting the final result, within the task's scope.
- Be honest about what was tested, what is incomplete, and what cannot be verified.

Do not add every item mechanically. Include only instructions that fit the task. For simple tasks, keep the process lightweight.

### 6. Make it ready to paste

The main upgraded prompt should be self-contained enough to copy into another AI chat without requiring the user to copy this conversation too. Include essential context supplied by the user. Avoid references like "as I said above" unless the relevant information is repeated inside the prompt.

Use the language that best fits the user's request. Usually preserve the language of the original prompt unless the user asks for another language or the target tool requires one.

### 7. Add filtered suggestions

After the main prompt, include a small section titled **Optional suggestions** only if there are genuinely useful additions that are not already required.

For each suggestion:
- Keep it short and specific.
- Explain the benefit in one sentence.
- Make clear it is optional.
- Do not mix it into the main prompt as a mandatory requirement.
- Do not include filler suggestions, generic best practices that add no value, or features unrelated to the request.

Prefer 0–5 suggestions. Zero is valid. If every useful improvement is already covered or no extra suggestion fits, omit the section entirely.

### 8. Final quality check

Before replying, check:
- The main goal remains unchanged.
- Every explicit requirement is included.
- No unsupported user preference, feature, platform, fact, or constraint was invented.
- Necessary details make the task more executable without bloating it.
- Optional ideas are relevant, limited, and clearly separated.
- The prompt is coherent, self-contained, and ready to paste.
- The requested output format is explicit.
- Claims about outcomes, usage savings, or model capabilities are not guaranteed without evidence.

## Default response format

Use this layout unless the user requests another format:

### Upgraded prompt
Provide the full prompt in a clean copyable block. Avoid commentary inside the prompt unless it is an instruction to the target AI.

### Optional suggestions
Include only relevant suggestions that are not already mandatory in the prompt. Omit this section when there are none.

### Brief note
Add one short note only if an assumption, ambiguity, or important limitation needs to be surfaced. Do not add a generic conclusion.

If the user asks for only the prompt, return only the upgraded prompt. If the user requests a file, create the requested file when tools allow it. If the user asks the AI to improve a prompt and execute it, do both in the requested order; otherwise, do not execute the improved prompt.

## Special cases

- **Extremely vague requests:** Improve what can be improved. Ask one question only if the missing answer changes the core deliverable and cannot be safely defaulted.
- **Conflicting requirements:** Preserve the explicit constraints and flag the conflict briefly instead of silently choosing one.
- **Sensitive or high-stakes tasks:** Do not make harmful or disallowed requests more actionable. Retain safety limits and steer toward a safe version when needed.
- **Prompts targeting a specific model:** Respect that model's known format only when supported by reliable context. Do not invent provider-specific syntax or claim prompt tricks can bypass system rules, policies, or usage limits.
- **Long prompts:** Optimize for signal, not sheer length. Remove duplication and organize requirements so the next model can find them.
- **Existing strong prompts:** Do not rewrite for the sake of rewriting. Make targeted improvements and explain briefly if only small changes are needed.
- **User asks for an “ultimate” prompt:** Interpret this as a request for completeness and clarity, not unrestricted feature expansion.
