---
name: web-apple-design
description: Apple Design Language for web applications. Use when building UI, choosing colors, typography, spacing, or component patterns for web projects that follow Apple's design philosophy (adapted from iOS HIG for web/Tailwind CSS).
---

# Apple Design Language for Web

## Purpose

Translates Apple's Human Interface Guidelines design philosophy into web-appropriate patterns using Tailwind CSS. Ensures visual consistency across iOS apps and web projects.

Use HIG as a clarity and interaction reference, not as a visual imitation.
Project-specific design systems, tokens, accessibility rules and domain skills
take precedence over every default below.

## When To Apply

Apply when the agent:

- Designs or modifies UI layouts
- Chooses colors, typography, or spacing
- Creates cards, forms, navigation, or data displays
- Implements dark mode
- Makes accessibility decisions

## Design Principles

### Typography
- Font: follow the project typography; prefer local/system delivery for
  privacy-sensitive products
- Code: JetBrains Mono
- Example sizes when the project has no established scale:
  - Page title: `text-3xl font-bold`
  - Section heading: `text-xl font-semibold` (20px)
  - Body: `text-base` (16px)
  - Caption: `text-sm text-muted` (14px)
- Line height: 1.5-1.6 for body text

### Colors (CSS Custom Properties)
- Reuse existing semantic CSS custom properties for background, surface,
  border, text, muted text, accent, warning, success and danger
- Do not introduce a second token vocabulary into an established project
- Preserve the project's accent color; do not default to Apple blue

### Dark Mode
- Follow the project's existing light/dark default and selector strategy
- Respect system preference where that matches the product decision
- All colors must work in both modes

### Spacing & Layout
- Card padding: `p-5` or `p-6` (20-24px)
- Section gaps: `gap-6` (24px)
- Card radius: `rounded-2xl` (16px) for large cards, `rounded-xl` (12px) for smaller
- Max content width: `max-w-6xl` centered
- Responsive grid: `grid-cols-1 md:grid-cols-2 lg:grid-cols-3`

### Components
- **Cards**: White/dark background, subtle shadow, rounded corners, no heavy borders
- **Badges**: Small, colored background with matching text (`bg-green-bg text-green`)
- **Buttons**: Existing project accent, clear states, rounded where established
- **Tables**: Clean, minimal borders, alternating row backgrounds optional
- **Navigation**: Sidebar on desktop (fixed), collapsible on mobile

### Shadows
- Card: `shadow-sm` to `shadow-md` (subtle, not heavy)
- Elevated: `shadow-lg` (modals, dropdowns)
- Dark mode: stronger shadows with higher opacity

### Animations
- Transition only the required properties; avoid `transition-all`
- Hover states: subtle opacity or background change
- No flashy animations — Apple-style restraint
- Respect `prefers-reduced-motion`

### Accessibility
- Target WCAG 2.2 AA
- Preserve visible focus, keyboard operation and semantic names
- Use at least 44 x 44 CSS-pixel touch targets for primary interactions
- Never communicate status by color alone

## Anti-Patterns
- No heavy borders or outlines on cards
- No bright saturated backgrounds
- No more than 2-3 colors per section
- No decorative elements without purpose
- No custom scrollbars unless essential
- No Apple trademark, product-page or platform imitation
