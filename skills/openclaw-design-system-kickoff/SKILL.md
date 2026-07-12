---
name: openclaw-design-system-kickoff
description: Defines a practical design-system starting point for new products or major redesigns. Use when a project needs coherent tokens, hierarchy, component families, and a visual direction before detailed screen implementation.
---

# OpenClaw Design System Kickoff

## Purpose

Use this skill when a project needs a coherent design direction before building or refactoring screens.

This skill helps turn vague taste goals into a usable system:

- visual direction
- tokens
- component families
- state patterns
- rollout priorities

It is for kickoff and alignment, not for endless design theorizing.

Default output language follows the user request language.

## When To Apply

Apply when:

- a new product surface is starting
- a redesign has become inconsistent across screens
- multiple contributors need one shared UI direction
- the user asks for a design system, style guide, or visual foundation

## Workflow

1. Capture the product context:
   - platform
   - audience
   - trust level
   - data density
   - existing brand constraints
2. Define three to five product keywords.
3. Translate them into concrete system choices:
   - typography
   - color system
   - spacing rhythm
   - radii
   - elevation
   - motion stance
4. Define the minimum viable component family:
   - page shells
   - cards
   - buttons
   - forms
   - data display
   - feedback states
5. Identify what should stay intentionally plain.
6. Produce a rollout order instead of trying to redesign everything at once.

## Deliverables

Prefer outputs in this shape:

- a one-page visual direction
- token recommendations
- component family list
- do / do not rules
- phased rollout suggestion

## Guardrails

- Do not invent a huge design system when three good primitives would do.
- Do not detach the system from the actual stack and product constraints.
- Do not overwrite an established product identity without reason.
- Do not make premium styling the goal; the goal is coherence plus usability.

## Relationships

This skill often comes before:

- `openclaw-web-premium-ui`
- `openclaw-ios-ui-curation`

It should also respect existing OpenClaw guardrails for:

- Apple-native products
- fintech or trust-sensitive flows
- analytics-heavy products

## Expected Output

Return a compact but implementation-oriented system draft.

If the project already has strong design conventions, prefer an incremental refresh over a full reset.
