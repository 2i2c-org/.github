# .github

This is a meta repository that defines some shared files that our other repositories inherit.

Below is a list of major files / functionality in this repository.

## `.github/ISSUE_TEMPLATE/` sync issue templates

Issue templates for other repositories. When these files changed, they are automatically synced to our other repositories.

- Syncing is done via [`.github/workflows/sync-issue-templates.yaml`](.github/workflows/sync-issue-templates.yaml).
- The issue templates are defined in [`.github/sync.yml`](.github/sync.yml).

## `.github/labels.yml` sync issue labels

We automatically synchronize a subset of issue labels across all of our major repositories.
This is done via a [**workflow_dispatch**](https://github.blog/changelog/2021-11-10-github-actions-input-types-for-manual-workflows/).

- The repositores and action is defined in [`.github/workflows/sync-labels.yml`](.github/workflows/sync-labels.yml).
- The labels are defined in [`.github/labels.yml`](.github/labels.yml).

## Reusable Workflow - Documentation link checks

We define a re-usable GitHub workflow to use Sphinx's `linkcheck` builder and open an issue if there are broken links. It is defined at [`.github/workflows/documentation-link-check.yaml`](.github/workflows/documentation-link-check.yaml).

## Pre-commit hooks

This repository uses the `prettier` pre-commit hook to standardize our YAML and markdown structure.
This ensures that when we sync files to other repositories, we do not create conflicts with `prettier` checks in each repository.
To install and run it, use these commands from the repository root:

```console
$ pre-commit install
$ pre-commit run -a
```
