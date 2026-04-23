# FNLLA Ecosystem Versioning Policy

## Purpose

Define a consistent release model across `github.com/fnlla` without forcing
artificially identical versions for every repository.

## Core Rule

Repositories should follow **aligned compatibility majors** and **independent
minor/patch release cadence**.

That means:

- Major versions align where there is direct runtime dependency coupling.
- Minor and patch versions are released independently per repository.
- Not every repository must have the same numeric tag at the same time.

## Recommended Strategy

1. Use SemVer for all public repositories.
2. Keep compatibility matrix explicit in release notes and README files.
3. Treat breaking changes as major bumps only in impacted repositories.
4. Keep branch aliases aligned for active major lines (for example `3.0.x-dev`).
5. Validate cross-repo constraints before tagging (starter, installer, packages).

## Packagist Scope Clarification

- **Publish on Packagist**: installable Composer packages (for example `fnlla/fnlla`, `fnlla/installer`).
- **Do not publish as package by default**: distribution/meta repositories that act
  as Composer repository indexes (for example `fnlla/packages`).

`fnlla/packages` is primarily a distribution hub (`repository/packages.json` +
dist archives). It should remain a Composer repository endpoint unless its role
changes into a standalone installable package.

## Practical Baseline for FNLLA

- `framework`, `packages`, `fnlla` should keep aligned major compatibility lines.
- `docs`, `quality`, `dev-env`, `fnlla-vs-code-extension` can release independently.
- Organization policy and community templates in `.github` may use their own cadence.
