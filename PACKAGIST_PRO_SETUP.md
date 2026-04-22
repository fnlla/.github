# Packagist Professional Setup (fnlla)

## Current Status (22 April 2026)

- `fnlla/fnlla`: published (`v3.0.6`), GitHub webhook active.
- `fnlla/installer`: published (`v1.0.0`), GitHub webhook active.
- `fnlla/framework`: intentionally not published on public Packagist (private source-of-truth repo).

## Mandatory Baseline

- Keep package ownership under the organization account (`fnlla`).
- Keep GitHub webhook on each Packagist package repo:
  `https://packagist.org/api/github`
- Publish tagged releases (`v*`) with changelog notes.
- Keep package README install instructions aligned with latest stable tag.

## Reliability Fallback

- Repos `fnlla/fnlla` and `fnlla/installer` include:
  `.github/workflows/packagist-fallback-update.yml`
- Configure repository secrets:
  - `PACKAGIST_USERNAME`
  - `PACKAGIST_API_TOKEN`
- Fallback workflow can be run manually or on tag push if webhook delivery ever fails.

## Verification Checklist

- New tag visible in Packagist p2 metadata within expected delay window.
- Dist URL resolves to GitHub archive reference for the same tag commit.
- `composer create-project fnlla/fnlla` works from a clean machine.
- `composer global require fnlla/installer` resolves latest stable installer tag.
