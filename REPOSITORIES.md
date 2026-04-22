# Fnlla Repository Map

## Developer-Facing Repositories

- `fnlla/fnlla`: starter application template for product teams.
- `fnlla/packages`: public Composer metadata and distribution archives.
- `fnlla/installer`: installer CLI (`fnlla new`) that wraps starter bootstrap.

## Maintainer-Facing Repository

- `fnlla/framework` (private): source-of-truth for framework and release governance.

## Dependency Flow

1. Product developers bootstrap from `fnlla/fnlla`.
2. Composer resolves `fnlla/*` packages through `fnlla/packages`.
3. Maintainers manage source and release policy in `fnlla/framework`.
4. Public package artifacts are refreshed in `fnlla/packages`.

## Governance

- Community defaults and templates live in `fnlla/.github`.
- `CODEOWNERS` is maintained per repository.
