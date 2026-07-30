# Contributing

Thanks for considering contributing to docker-infra.

## Getting started

1. Fork the repository on Gitea.
2. Clone your fork locally.
3. Create a branch for your changes.

## Branch naming

Use the format `<type>/<short-description>`:

| Type     | Usage                             |
| -------- | --------------------------------- |
| feature  | New functionality                 |
| fix      | Bug fix                           |
| docs     | Documentation changes             |
| chore    | Tooling, dependencies, maintenance |

Examples: `feature/add-postgres-compose`, `docs/update-readme`.

## Commit messages

Follow the [Conventional Commits](https://www.conventionalcommits.org/) format:

```
<type>(<scope>): <description>
```

Keep the subject line under 50 characters. Use the imperative mood
("add feature", not "added feature").

## Pull requests

- Keep changes focused — one concern per pull request.
- Update or add documentation if your change affects usage.
- Ensure your branch is up to date with `main` before opening a PR.

## Code style

- Use British English spelling in all documentation and comments.
- Follow the existing style of the files you are editing.
- End YAML files with a trailing newline.
