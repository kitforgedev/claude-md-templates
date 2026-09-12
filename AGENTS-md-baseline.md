# AGENTS.md baseline

Single source of truth for every coding agent that touches this repo (Codex, Amp, Jules, Claude Code via @import, Cursor via .cursor/rules pointer).

## Build and test
- Install: `pnpm install`
- Build: `pnpm -r build`
- Test: `pnpm -r test`
- Lint: `pnpm -r lint`

## Conventions
- TypeScript strict mode. No new `any`.
- Conventional commits: `feat:`, `fix:`, `chore:`.
- Tests live next to source: `foo.ts` -> `foo.test.ts`.
- Never edit generated files: `dist/`, `*.generated.ts`, lockfiles by hand.

## Boundaries
- Do not force-push or amend published commits.
- Do not commit secrets. `.env` files are never read or printed.
- Database migrations are additive only; no drops without a human.
- Ask before publishing, deploying, or pushing to a shared branch.

## Where things live
- `packages/api` - backend service
- `packages/web` - frontend
- `docs/` - architecture and runbooks (read on demand, not upfront)

## Claude Code / Cursor notes
- CLAUDE.md imports this file with `@AGENTS.md` and adds tool-specific rules only.
- Cursor: keep `.cursor/rules/project.mdc` as a short pointer to this file.

