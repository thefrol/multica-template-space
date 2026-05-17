# Multica Template Space

A production-ready workspace template for Multica.

## Usage

### Create a new workspace from this template

```bash
multica-template-apply https://github.com/thefrol/multica-template-space --create-workspace
```

### Dry-run to preview changes

```bash
multica-template-apply https://github.com/thefrol/multica-template-space --dry-run
```

### Apply to an existing workspace

```bash
multica-template-apply https://github.com/thefrol/multica-template-space --workspace-id <uuid>
```

## Templates

| Template | Path | Description |
|----------|------|-------------|
| **Full** | *(root)* | Complete workspace with labels, skills, agents, squads, and autopilots |
| **Minimal** | `minimal/` | Workspace metadata, labels, and skills only |
| **Labels Only** | `labels-only/` | Just labels — safe for any workspace |

### Minimal template

```bash
multica-template-apply https://github.com/thefrol/multica-template-space/minimal --create-workspace
```

### Labels-only template

```bash
multica-template-apply https://github.com/thefrol/multica-template-space/labels-only --workspace-id <uuid>
```

## What's included

- **Labels**: bug, feature, docs, infra, security, design
- **Skills**: code-review, security-audit, on-call-runbook
- **Agents**: auto-coder, security-guardian, devops-engineer, product-manager
- **Squads**: platform-squad, product-squad, security-squad
- **Autopilots**: daily-security-scan, weekly-backlog-grooming, weekly-on-call-review

## New workspace limitation

Creating a **new** workspace via `--create-workspace` works for workspace metadata, labels, and skills. **Agents require a runtime** to be registered in the target workspace first. If you see `ERROR: no runtimes available in target workspace`, create the workspace first, register a runtime via the web UI, then re-apply the template.
