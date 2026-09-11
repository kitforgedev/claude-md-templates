# CLAUDE.md - Your Project (Go)

## Ground rules

- Test first: write or update the failing test before changing behavior.
- Stay in scope: touch only the files the task requires. Ask before refactoring anything outside the diff.
- Small commits: one logical change per commit, conventional-commit message.
- Never force-push, never commit directly to main, never skip hooks.

## Code style

- Errors are values: check every error, wrap with context using fmt.Errorf and %w.
- No global mutable state. Dependencies injected via constructors.
- Interfaces live at the consumer, not the provider.
- Context passed as first argument to every function that does I/O.

## Definition of done

- [ ] Tests pass (`go test ./...`)
- [ ] Lint and typecheck clean (`go vet ./... && staticcheck ./...`)
- [ ] New code follows the style rules above
- [ ] New public functions have a doc comment
- [ ] Diff self-reviewed and findings addressed
