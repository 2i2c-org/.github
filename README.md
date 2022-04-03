# .github

This is a meta repository that defines some shared files that our other repositories inherit.

## Files used in this repository

Below is a quick list of these files:

- `.github/ISSUE_TEMPLATE/`: Issue templates for other repositories. When these files changed, they are automatically synced to our other repositories via [this GitHub action](.github/workflows/sync-issue-templates.yaml). See the comments in those actions for more details.

## Pre-commit hooks

This repository uses the `prettier` pre-commit hook to standardize our YAML and markdown structure.
This ensures that when we sync files to other repositories, we do not create conflicts with `prettier` checks in each repository.
To install and run it, use these commands from the repository root:

```console
$ pre-commit install
$ pre-commit run -a
```
