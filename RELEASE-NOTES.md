# Pueblo CLI 0.4.0

## 0.4.0

Universal, signed, Apple-notarized macOS feature release for Apple silicon and Intel.

- Create and edit leads through Pueblo's app-owned validation and persistence paths.
- Apply bounded multi-record edits across clients, contacts, leads, engagements, and journal notes. Use `pueblo batch-edit --dry-run` to preview before saving.
- Preview and explicitly confirm deletion of clients, contacts, leads, engagements, and journal entries using stable UUIDs. A current preview token does not replace user authorization.
- Keep all reads and writes inside the authenticated running Pueblo app; the CLI does not access its database or CloudKit directly.

These new operations require a matching Pueblo macOS app build. Earlier app builds return `feature_unavailable` for unsupported operations. See [installation and compatibility details](INSTALL.md).

### 0.3.1

Universal, signed, Apple-notarized macOS hotfix for Apple silicon and Intel.

- Fix `pueblo pair` for the sandboxed signed CLI by reading the code with terminal echo disabled in the installed launcher and forwarding it over standard input.
- Upgrade from 0.3.0 automatically replaces the previous command symlink with the launcher while preserving the prior signed app bundle for rollback.
- Keep all reads and writes inside the authenticated running Pueblo app; the CLI does not access its database or CloudKit directly.
- Preserve checklist and existing list, search, detail, create, and edit operations.

See [installation and compatibility details](INSTALL.md).

## 0.3.0

Universal, signed, Apple-notarized macOS release for Apple silicon and Intel.

- Manage checklist items through Pueblo with `pueblo todo list|add|update|complete|reopen|delete`.
- Delete one checklist item by UUID; CRM entity deletion remains unavailable.
- Keep all reads and writes inside the authenticated running Pueblo app; the CLI does not access its database or CloudKit directly.
- Include per-user installation, upgrade rollback, and uninstall scripts.
- Preserve existing list, search, detail, create, and edit operations.

Checklist commands require a Pueblo macOS app build that includes the checklist CLI service. Earlier app builds continue to support their existing operations and return `feature_unavailable` for checklist commands. See [installation and compatibility details](INSTALL.md).
