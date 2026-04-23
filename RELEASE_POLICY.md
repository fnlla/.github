# FNLLA Release Policy

## Objective

Establish one consistent release process across FNLLA repositories while preserving
independent release cadence per repository.

## Tag Format

- Stable: `vX.Y.Z`
- Pre-release allowed: `vX.Y.Z-rc.1`, `vX.Y.Z-beta.2`
- Build metadata allowed: `vX.Y.Z+build.4`

## Standard Release Flow

1. Prepare changelog/notes for the target version.
2. Trigger release via either:
   - Tag push (`git tag vX.Y.Z && git push origin vX.Y.Z`), or
   - Manual workflow dispatch with version input and `create_tag=true`.
3. Reusable workflow validates tag format.
4. Repository publishes GitHub Release using generated notes or changelog notes.

## Reusable Workflow

All repositories should use:

- `.github/.github/workflows/reusable-release.yml`

Supported features:

- Optional automatic tag creation.
- Optional changelog section enforcement.
- Optional release notes extraction from changelog.
- Optional artifact attachments.

## Repository Classes

- Runtime and tooling repos (`fnlla`, `installer`, `quality`, `dev-env`, `fnlla-vs-code-extension`) use SemVer with independent minor/patch cadence.
- Distribution/index repos (`packages`) can publish release tags for governance and traceability even when not Packagist-installable.
- Documentation and website repos (`docs`, `www`) may release content snapshots using the same workflow.

## Branch and PR Guardrails

- Releases happen from protected `main`.
- PR checks and approvals are required before merge.
- Release workflow is write-scoped only to repository contents.
