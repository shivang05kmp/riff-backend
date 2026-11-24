# Git workflow
- `main` is protected: every change lands through a PR, squash-merged.
- Branch names: `feat/…`, `fix/…`, `docs/…`, `chore/…`.
- Commit / PR titles follow Conventional Commits: `type(scope): summary`.
- Before opening a PR: `git fetch && git rebase origin/main` (only on my own branch).
- After a rebase: `git push --force-with-lease` (never plain --force, never on main).
