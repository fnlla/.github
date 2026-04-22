# Fnlla

Production-focused PHP framework ecosystem with a public developer experience and
a private source-of-truth core.

## Core Repositories

| Repository | Visibility | Role |
|---|---|---|
| `fnlla/fnlla` | Public | Official starter application (`composer create-project`) |
| `fnlla/packages` | Public | Composer package distribution hub (`repository/packages.json` + `repository/dist/*`) |
| `fnlla/framework` | Private | Source-of-truth framework and maintainer release control plane |
| `fnlla/installer` | Public | Installer CLI (`fnlla new`) |
| `fnlla/.github` | Public | Organization-wide community health defaults |

## Install Paths

### Starter (Composer)

```bash
composer create-project fnlla/fnlla my-app
```

### Starter (Installer CLI)

```bash
composer global config repositories.fnlla-installer vcs https://github.com/fnlla/installer
composer global require fnlla/installer:dev-main
fnlla new my-app
```

## Distribution Model

- Public runtime dependencies are served from `fnlla/packages`.
- Starter bootstrap remains public and frictionless.
- Framework source stays private for controlled release management.

## Security

- Vulnerability reports: `security@fnlla.co.uk`
- Security policy defaults: `fnlla/.github/SECURITY.md`
