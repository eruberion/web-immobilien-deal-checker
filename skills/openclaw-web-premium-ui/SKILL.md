---
name: openclaw-web-premium-ui
description: Curates premium, product-disciplined web UI for React/Vite/Tailwind projects. Use when redesigning or polishing web screens that need stronger visual identity than the baseline web style, while preserving readability, accessibility, and product fit.
---

# OpenClaw Web Premium UI

## Purpose

Use this skill to raise the visual finish of OpenClaw web projects without drifting into generic template output or design-for-design's-sake.

This skill is a curation layer, not a replacement for:

- `react-vite-typescript`
- `web-apple-design`

Default output language follows the user request language.

## When To Apply

Apply when the task involves:

- redesigning or polishing web UI
- defining visual direction for a new page or feature
- improving layout rhythm, hierarchy, typography, or component finish
- making a web product feel more intentional, premium, and less boilerplate

Use especially for:

- landing pages
- dashboards
- settings and overview surfaces
- empty states and marketing-adjacent product areas

## Do Not Apply By Default

Do not use this skill as the primary driver when:

- the task is backend-only or logic-only
- a project already has a rigid external design system that must be followed literally
- the screen is primarily about dense tables or raw data inspection
- the flow is trust-critical and clarity must win over expression

For finance-adjacent or analytics-heavy screens:

- readability beats novelty
- hierarchy beats decoration
- state clarity beats visual drama

## Default Workflow

1. Baseline the current screen or target page.
2. Identify the product mode:
   - app-like
   - dashboard-like
   - landing-like
   - hybrid
3. Define one clear visual direction before changing components.
4. Improve hierarchy first:
   - layout
   - spacing
   - typography
   - grouping
5. Add premium finish only where it supports comprehension:
   - background treatment
   - accent color system
   - motion
   - detail components
6. Validate accessibility, responsiveness, and product fit.

## Curation Rules

- Prefer a clear visual thesis over a pile of trendy details.
- Use CSS custom properties for color and spacing decisions when possible.
- Avoid flat, default-looking surfaces if the page needs more atmosphere.
- Use motion sparingly and intentionally:
  - page-entry
  - staggered reveal
  - section emphasis
- Typography should feel chosen, not accidental.
- Components should look related across the page, not copied from mixed libraries.

## Guardrails

- Do not default to purple-on-white aesthetics.
- Do not rely on generic SaaS dashboards without project-specific character.
- Do not reduce contrast, tap targets, or responsive behavior for style.
- Do not add decorative motion to critical actions or forms.
- Do not overuse gradients, glass, or blur where they hurt legibility.

## Project Fit

Best fit:

- Pulsview
- Altersvorsorgeplanung

Selective fit:

- sg1920-stammheim public-facing pages

Use with extra restraint:

- EnergyLens web-like dashboard surfaces in docs or prototypes

## Expected Output

Return one or more of:

- a concise visual direction
- a layout and component plan
- concrete CSS/Tailwind guidance
- a focused redesign proposal
- implementation-ready UI changes

Always include a short self-check for:

- readability
- responsiveness
- accessibility
- product fit
