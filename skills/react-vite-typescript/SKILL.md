---
name: react-vite-typescript
description: Development rules for React + Vite + TypeScript web projects. Use when building UI components, managing state, configuring builds, writing tests, or any frontend development in the React/Vite/TypeScript stack with Tailwind CSS.
---

# React / Vite / TypeScript Web Development

## Purpose

Use this skill to write correct, maintainable, and performant React web applications using Vite as build tool, TypeScript in strict mode, and Tailwind CSS for styling.

## When To Apply

Apply when the agent:

- Creates or modifies React components
- Changes routing (React Router v7)
- Modifies state management (Zustand or React hooks)
- Adds or modifies TypeScript types/interfaces
- Changes Vite configuration or build setup
- Writes or modifies tests (Vitest)
- Adjusts Tailwind CSS classes or configuration
- Changes `package.json` dependencies

## Risk Classification

HIGH:
- Authentication or token handling (if applicable)
- Financial calculations or sensitive data processing
- Build configuration changes affecting production output

MEDIUM:
- State management changes (Zustand stores)
- Routing changes
- New dependency additions

LOW:
- UI component changes
- Styling adjustments
- Test additions

## Architecture Rules

### TypeScript
- `strict: true` in `tsconfig.json` — no exceptions
- Never use `any`. Use `unknown` with type guards if the type is truly uncertain
- Types belong in `src/types/` as named exports
- Prefer interfaces over type aliases for object shapes

### Components
- One component per file
- Named exports only (no default exports)
- Props interfaces co-located or in `src/types/`
- Use functional components with hooks
- Prefer composition over prop drilling

### State Management
- Zustand for global/persistent state
- React hooks (`useState`, `useReducer`) for local component state
- localStorage persistence via Zustand middleware where needed

### Styling
- Tailwind CSS v4 utility classes
- Dark mode via `dark:` prefix (dark-first design)
- No inline styles unless dynamic values require them
- Apple Design Tokens where established in the project

### Build & Dev
- Vite dev server with HMR
- `npm run build` must pass without errors before any commit
- `npm run type-check` (if configured) must pass
- Bundle size awareness — avoid large dependencies

### Testing
- Vitest for unit tests
- Tests in `__tests__/` directories or `*.test.ts` files
- Test business logic and calculations, not UI rendering details

### File Structure
```
src/
├── components/    # React components (grouped by feature)
├── hooks/         # Custom React hooks
├── lib/           # Business logic, utilities, calculations
├── types/         # TypeScript type definitions
├── i18n/          # Translations (if multilingual)
├── App.tsx        # Root component
├── main.tsx       # Entry point
└── index.css      # Global styles + Tailwind imports
```

## Quality Checklist

Before completing any task:
- [ ] No TypeScript errors (`npm run type-check` or build)
- [ ] No `any` types introduced
- [ ] Components use named exports
- [ ] New dependencies justified and minimal
- [ ] Responsive design considered (mobile + desktop)
- [ ] Dark mode classes applied where visible
