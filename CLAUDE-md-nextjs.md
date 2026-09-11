# CLAUDE.md - Next.js App Router (full example)

A complete, production-shaped CLAUDE.md for a Next.js 15 App Router project. Trim the sections that don't apply; every line should earn its context budget.

## Commands

- Dev: `pnpm dev`
- Build: `pnpm build` (must pass before any PR)
- Test: `pnpm test` (unit, vitest) / `pnpm test:e2e` (playwright, slow - run only before merge)
- Lint: `pnpm lint` / Format: `pnpm format`

## Architecture

- App Router only. No pages/ directory, ever.
- Server Components by default. Add 'use client' only when you need state, effects, or browser APIs - and say why in a comment.
- Data fetching lives in Server Components or Route Handlers. No client-side fetch for initial page data.
- Shared UI in `components/ui/` (design system), feature components in `components/features/<name>/`.
- Server Actions in `app/<route>/actions.ts`, colocated with the route that uses them.

## Hard rules

- NEVER add a dependency without asking. List is frozen.
- NEVER edit `.env*`, `pnpm-lock.yaml`, or files under `migrations/`.
- No `any` in TypeScript. If the type is hard, ask - don't cast.
- Don't reformat or reorder code you didn't change.

## Conventions

- Named exports for components. Default exports only for route files (Next requires them).
- `cn()` helper for conditional classes (in `lib/utils.ts`).
- Errors: Route Handlers return `NextResponse.json({ error }, { status })`; Server Actions throw typed errors from `lib/errors.ts`.
- Dates: store UTC ISO strings, format client-side with `lib/date.ts`.

## Definition of done

1. `pnpm build` and `pnpm test` pass - paste the output.
2. New UI renders in both light and dark mode.
3. New data fetching handles loading and error states.
4. Commit message follows conventional commits.

## When unsure

Stop and ask. A two-line question is cheaper than a 200-line wrong direction.
