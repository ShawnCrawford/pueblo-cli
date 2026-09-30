# Pueblo CLI 0.2.0

Universal, signed, Apple-notarized macOS release for Apple silicon and Intel.

- Read lists and details for clients, contacts, leads, engagements, and journal entries; search supported record types.
- Create and edit clients, contacts, engagements, and journal user notes using Pueblo's app-owned validation and relationship logic.
- Preserve authenticated communication with the running Pueblo app; no direct database or CloudKit access.
- Include per-user installation, upgrade rollback, and uninstall scripts.
- Pairing codes expire after five minutes and are not echoed in Terminal.

Leads are read-only. Delete operations and `todo list` are unsupported. The new create/edit operations require a compatible Pueblo macOS app release with the 0.2.0 service protocol. See [installation and compatibility details](INSTALL.md).
