# Pueblo CLI 0.3.0

Universal, signed, Apple-notarized macOS release for Apple silicon and Intel.

- Manage checklist items through Pueblo with `pueblo todo list|add|update|complete|reopen|delete`.
- Delete one checklist item by UUID; CRM entity deletion remains unavailable.
- Keep all reads and writes inside the authenticated running Pueblo app; the CLI does not access its database or CloudKit directly.
- Include per-user installation, upgrade rollback, and uninstall scripts.
- Preserve existing list, search, detail, create, and edit operations.

Checklist commands require a Pueblo macOS app build that includes the checklist CLI service. Earlier app builds continue to support their existing operations and return `feature_unavailable` for checklist commands. See [installation and compatibility details](INSTALL.md).
