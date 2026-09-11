# CLAUDE.md - Your Project (TypeScript/Node)

## Ground rules

- Test first: write or update the failing test before changing behavior.
- Stay in scope: touch only the files the task requires. Ask before refactoring anything outside the diff.
- Small commits: one logical change per commit, conventional-commit message.
- Never force-push, never commit directly to main, never skip hooks.

## Code style

- TypeScript strict mode. No `any` without a comment explaining why.
- Named exports for modules, default exports for pages/routes only.
- Errors: throw typed errors from the domain layer, catch at the boundary.
- Async: no floating promises. Every promise is awaited or returned.

## Definition of done

- [ ] Tests pass (`npm test`)
- [ ] Lint and typecheck clean (`npm run check`)
- [ ] New code follows the style rules above
- [ ] New public functions have a doc comment
- [ ] Diff self-reviewed and findings addressed
