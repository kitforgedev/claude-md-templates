# CLAUDE.md - Your Project (Python/FastAPI)

## Ground rules

- Test first: write or update the failing test before changing behavior.
- Stay in scope: touch only the files the task requires. Ask before refactoring anything outside the diff.
- Small commits: one logical change per commit, conventional-commit message.
- Never force-push, never commit directly to main, never skip hooks.

## Code style

- Type hints on all public functions. No `Any` without a comment explaining why.
- Pydantic models at the API boundary; domain logic stays framework-free.
- Errors: raise domain exceptions, map to HTTP at the router layer.
- Async: use async endpoints only for I/O-bound work; no fire-and-forget tasks without tracking.

## Definition of done

- [ ] Tests pass (`pytest`)
- [ ] Lint and typecheck clean (`ruff check . && mypy .`)
- [ ] New code follows the style rules above
- [ ] New public functions have a doc comment
- [ ] Diff self-reviewed and findings addressed
