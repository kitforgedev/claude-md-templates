# CLAUDE.md - Your Project (React/Next.js)

## Ground rules

- Test first: write or update the failing test before changing behavior.
- Stay in scope: touch only the files the task requires. Ask before refactoring anything outside the diff.
- Small commits: one logical change per commit, conventional-commit message.
- Never force-push, never commit directly to main, never skip hooks.

## Code style

- Server components by default; client components only where interactivity requires.
- No `any` in TypeScript. Props get explicit interfaces.
- Data fetching in server components or route handlers, never in useEffect.
- Errors: error.tsx at route boundaries, typed errors from server actions.

## Definition of done

- [ ] Tests pass (`npm test`)
- [ ] Lint and typecheck clean (`npm run check`)
- [ ] New code follows the style rules above
- [ ] New public functions have a doc comment
- [ ] Diff self-reviewed and findings addressed
