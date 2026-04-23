# FNLLA Organization Standards

![FNLLA Hero](./profile/assets/fnlla-hero.svg)

![FNLLA Logo](./profile/assets/fnlla-logo.svg)

**ORCHESTRATED**

This repository is the governance and standards control plane for `github.com/fnlla`.
It defines the default operating model used across FNLLA repositories, from community
health and contribution templates to synchronization workflows and release policy
references.

## What This Repository Provides

- Security policy (`SECURITY.md`)
- Support policy (`SUPPORT.md`)
- Contribution guidelines (`CONTRIBUTING.md`)
- Code of conduct (`CODE_OF_CONDUCT.md`)
- Issue templates (`.github/ISSUE_TEMPLATE/*`)
- Pull request template (`PULL_REQUEST_TEMPLATE.md`)
- Reusable sync workflow (`.github/workflows/reusable-sync-community-health.yml`)
- Reusable release workflow (`.github/workflows/reusable-release.yml`)
- Reusable CodeQL workflow (`.github/workflows/reusable-codeql.yml`)
- Repository map (`REPOSITORIES.md`)
- Packagist operations baseline (`PACKAGIST_PRO_SETUP.md`)
- Ecosystem versioning policy (`VERSIONING_POLICY.md`)
- Ecosystem release policy (`RELEASE_POLICY.md`)
- Security response SLA (`SECURITY_RESPONSE_SLA.md`)

## Governance Model

- Repository-level files may override org defaults where justified by scope.
- `CODEOWNERS` is maintained per repository for explicit accountability.
- Standards can be propagated through reusable workflows from this repository.
- Policy updates are treated as platform changes and reviewed accordingly.

## Ecosystem Overview

![FNLLA Ecosystem](./profile/assets/fnlla-ecosystem.svg)

## Packagist Baseline

- Public installable packages should be registered in Packagist.
- Distribution-only repositories are not automatically Packagist candidates.
- See `PACKAGIST_PRO_SETUP.md` for operational checklist and fallback workflow.

## Versioning Baseline

FNLLA repositories do not need identical tag numbers at every release. Instead:

1. Compatibility majors are aligned where repositories integrate directly.
2. Each repository releases independently at minor/patch level.
3. Cross-repo compatibility is tracked through constraints, changelogs, and release notes.

Details: `VERSIONING_POLICY.md`.

## Release Baseline

All FNLLA repositories should publish releases through the reusable workflow in this repository,
with consistent tag validation and optional changelog enforcement.

Details: `RELEASE_POLICY.md`.
