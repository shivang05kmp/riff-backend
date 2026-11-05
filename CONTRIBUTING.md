# Contributing

How work moves into `main`. These rules apply to everyone, Claude included.

## The main branch

- `main` always works: it builds, the tests pass, and it runs.
- Nobody commits to `main` directly. All work goes through a short-lived branch and a pull request (PR).
- After merging, delete the branch. Old branches are clutter.

## Branch names

Format: `<type>/<short-description>`, all lowercase, words joined with hyphens.
Once Riff is split into services (Week 4), start the description with the service: `<type>/<service>-<short-description>`.

| Type | Use it for |
| --- | --- |
| `feat` | a new feature or endpoint |
| `fix` | a bug fix |
| `docs` | documentation only |
| `test` | adding or fixing tests only |
| `refactor` | changing code without changing behaviour |
| `perf` | a performance improvement |
| `chore` | setup, dependencies, config, Docker Compose |
| `ci` | GitHub Actions workflows |

Examples:

```
docs/repo-scaffold
chore/postgres-compose
feat/spring-boot-skeleton
feat/track-upload
fix/playlist-n-plus-one
feat/catalog-track-search      (after the service split)
ci/build-and-test
```

One branch covers one topic. If a plan day has two separate pieces, use two branches.

## Commit messages

Use [Conventional Commits](https://www.conventionalcommits.org/): `<type>(<scope>): <what changed, imperative mood>`.
The scope is optional: an area such as `tracks`, `auth` or `playlists`, or a service name after Week 4.

```
feat(tracks): add POST /tracks upload endpoint
fix(playlists): fetch playlist tracks in one query
docs: add branching rules
```

Write the subject as if it finishes the sentence "This commit will …". Keep it under 72 characters.

## Pull requests

1. Push your branch and open a PR into `main`.
2. Title: the same style as a commit message. Add the plan day if there is one, for example `feat: Spring Boot skeleton [Day 2]`.
3. Description: what changed, why, and how you tested it.
4. Merge with **Squash and merge**, so each PR becomes one commit on `main`.
5. Delete the branch.

## Releases

Each week of the plan ends with a tag on `main`, for example `v0.1.0` after Week 1.
