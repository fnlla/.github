# Fnlla Community Health Defaults

This repository provides organization-wide default community health files for
`github.com/fnlla` repositories.

Included defaults:

- Security policy (`SECURITY.md`)
- Support policy (`SUPPORT.md`)
- Contribution guidelines (`CONTRIBUTING.md`)
- Code of conduct (`CODE_OF_CONDUCT.md`)
- Issue templates (`.github/ISSUE_TEMPLATE/*`)
- Pull request template (`PULL_REQUEST_TEMPLATE.md`)
- Reusable sync workflow (`.github/workflows/reusable-sync-community-health.yml`)

Notes:

- Repository-level files override these defaults.
- `CODEOWNERS` is maintained per repository.
- Repositories can auto-sync these defaults by calling the reusable workflow from this repo.
- Packagist operational checklist lives in `PACKAGIST_PRO_SETUP.md`.
