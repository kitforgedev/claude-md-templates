# CLAUDE.md - Your Project (Rust)

## Ground rules

- Test first: write or update the failing test before changing behavior.
- Stay in scope: touch only the files the task requires. Ask before refactoring anything outside the diff.
- Small commits: one logical change per commit, conventional-commit message.
- Never force-push, never commit directly to main, never skip hooks.

## Code style

- No `unwrap()` or `expect()` outside tests. Use `?` with thiserror error types.
- Prefer borrowing over cloning. Clone only with a comment explaining why.
- Unsafe only with a safety comment and a bounding invariant.
- Public API items get doc comments with examples that compile.

## Definition of done

- [ ] Tests pass (`cargo test`)
- [ ] Lint and typecheck clean (`cargo clippy -- -D warnings && cargo fmt --check`)
- [ ] New code follows the style rules above
- [ ] New public functions have a doc comment
- [ ] Diff self-reviewed and findings addressed
