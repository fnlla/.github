# Fnlla Repository Map

## Developer-Facing Repositories

- `fnlla/fnlla`: starter application template for product teams.
- `fnlla/packages`: public Composer metadata and distribution archives.
- `fnlla/installer`: installer CLI (`fnlla new`) that wraps starter bootstrap.
- `fnlla/docs`: official versioned documentation portal.
- `fnlla/quality`: official style and QA tooling.
- `fnlla/dev-env`: official Docker-first local development runtime.
- `fnlla/fnlla-vs-code-extension`: official VS Code integration for FNLLA projects.

## Maintainer-Facing Repository

- `fnlla/framework` (private): source-of-truth for framework and release governance.

## Dependency Flow

1. Product developers bootstrap from `fnlla/fnlla`.
2. Composer resolves `fnlla/*` packages through `fnlla/packages`.
3. Maintainers manage source and release policy in `fnlla/framework`.
4. Public package artifacts are refreshed in `fnlla/packages`.
5. Docs lifecycle is published independently from `fnlla/docs`.
6. Local runtime standards are versioned in `fnlla/dev-env`.
7. Style/QA policy is distributed via `fnlla/quality`.

## Governance

- Community defaults and templates live in `fnlla/.github`.
- `CODEOWNERS` is maintained per repository.
- Community policy files are auto-synced by reusable workflow:
  `fnlla/.github/.github/workflows/reusable-sync-community-health.yml`.

## Registry Strategy

- Public packages intended for open usage (for example `fnlla/fnlla`, `fnlla/installer`) are published on Packagist.
- `fnlla/framework` stays private on GitHub and is not published on public Packagist.
- Runtime package resolution for starter apps is handled by `fnlla/packages` composer repository metadata.
