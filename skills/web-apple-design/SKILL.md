---
name: web-apple-design
description: Apple Design Language for web applications. Use when building UI, choosing colors, typography, spacing, or component patterns for web projects that follow Apple's design philosophy (adapted from iOS HIG for web/Tailwind CSS).
---

# Apple Design Language for Web

## Purpose

Translates Apple's Human Interface Guidelines design philosophy into web-appropriate patterns using Tailwind CSS. Ensures visual consistency across iOS apps and web projects.

## When To Apply

Apply when the agent:

- Designs or modifies UI layouts
- Chooses colors, typography, or spacing
- Creates cards, forms, navigation, or data displays
- Implements dark mode
- Makes accessibility decisions

## Design Principles

### Typography
- Font: Inter (primary), system-ui fallback
- Code: JetBrains Mono
- Sizes follow Apple's type scale:
  - Page title: `text-3xl font-bold` (28px)
  - Section heading: `text-xl font-semibold` (20px)
  - Body: `text-base` (16px)
  - Caption: `text-sm text-muted` (14px)
- Line height: 1.5-1.6 for body text

### Colors (CSS Custom Properties)
- Background: `--bg-page`, `--bg-secondary`, `--bg-card`
- Text: `--text-heading`, `--text-body`, `--text-secondary`, `--text-muted`
- Accents: `--blue`, `--green`, `--orange`, `--red`, `--purple`
- Each accent has a `-bg` variant for subtle backgrounds
- Borders: `--border` (subtle), `--border-strong` (visible)

### Dark Mode
- Dark-first approach
- Toggle between light/dark with `[data-theme="dark"]`
- Store preference in localStorage, respect system preference
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
- **Buttons**: Primary blue, rounded, no heavy borders
- **Tables**: Clean, minimal borders, alternating row backgrounds optional
- **Navigation**: Sidebar on desktop (fixed), collapsible on mobile

### Shadows
- Card: `shadow-sm` to `shadow-md` (subtle, not heavy)
- Elevated: `shadow-lg` (modals, dropdowns)
- Dark mode: stronger shadows with higher opacity

### Animations
- Transitions: `transition-all duration-200 ease`
- Hover states: subtle opacity or background change
- No flashy animations — Apple-style restraint

## Anti-Patterns
- No heavy borders or outlines on cards
- No bright saturated backgrounds
- No more than 2-3 colors per section
- No decorative elements without purpose
- No custom scrollbars unless essential
