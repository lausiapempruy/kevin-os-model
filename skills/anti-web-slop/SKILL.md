---
name: anti-web-slop
description: Enforce zero AI-generated and generic web design slop when building any website, landing page, app UI, dashboard, or marketing site. Use in build mode, design mode, UI generation, landing page creation, or any frontend task. Triggers on build, design, website, landing, hero, UI, app, SaaS, dashboard, or when user asks for clean/non-generic/non-AI look. Applies strict anti-slop filters to all outputs.
---

# Anti Web Slop

Prevent AI slop and generic web design patterns. Every UI, landing page, or app interface you produce must pass these filters. No exceptions in build mode.

## Core Rules

1. **Zero tolerance for AI slop** — Never ship patterns from `references/ai-slop.md`.
2. **Strong preference against generic slop** — Avoid patterns from `references/generic-slop.md` unless the user explicitly requests a conventional look or there is a strong product reason.
3. **Claims must be real** — Never invent metrics, user counts, testimonials, logos of partners, or "as featured in". If data is unknown, omit it or use honest placeholders that the user can replace.
4. **Filter before output** — Before finalizing any design or code, mentally scan against both checklists. If a pattern matches, redesign it.

## When to Activate Fully

- User says "build", "buat", "design", "landing page", "website", "app", "dashboard", "UI", "SaaS", "hero section", or similar.
- Any request that produces frontend code, visual design, or marketing copy for a product.
- When the user asks for something that looks premium, distinctive, or "not AI-looking".

## Decision Filter (avoid false positives)

Apply these before flagging something as slop:

- **Intentional & distinctive** → allowed (even if it resembles a pattern).
- **User explicitly requested** the pattern → allowed.
- **Strong product/brand reason** (e.g. real partner logos, real metrics with source) → allowed.
- **Accidental or default look** → rewrite.
- **Copy feels like it was written by AI** (vague, buzzwordy, em-dash heavy) → rewrite in plain, specific language.

If unsure, prefer the more distinctive, less common choice.

## Required Workflow

When producing any web/UI output:

1. Read the relevant reference if needed:
   - `references/ai-slop.md` — 50 AI-specific anti-patterns
   - `references/generic-slop.md` — 50 common web design anti-patterns
2. Design or code with the lists in mind from the start (prevention > cure).
3. Self-audit the final output against both lists.
4. For any remaining match, replace with a more intentional alternative.
5. Ensure all social proof, metrics, testimonials, and partner claims are either real or clearly marked as placeholders for the user.

## Output Principles

- Prefer sharp edges, unexpected layouts, strong typography contrast, and limited color palettes with personality over safe rounded cards and blue gradients.
- Write copy that is specific to the product. Avoid vague inspirational language.
- Make interactive elements actually work or clearly mark them as static.
- Mobile must be clean. No horizontal scroll, no overlapping elements.
- Favicon, Open Graph, and basic legal pages are not optional for real projects.
- One strong visual idea is better than ten generic polish effects.

## Quick Anti-Slop Defaults

- No blue→purple gradients.
- No neon glow ambient blobs on dark backgrounds.
- No floating "AI-powered" badges above the hero.
- No em-dash spam.
- No "revolutionize your workflow" language.
- No fake numbers or fake faces.
- No forced bento grids.
- No shadcn defaults without brand customization.
- No 3-column pricing with "Most Popular" middle card unless the product truly needs it and is customized.
- Prefer real custom domain thinking even in prototypes (use example.com style, not *.vercel.app in final copy).

Keep the output honest, distinctive, and human.