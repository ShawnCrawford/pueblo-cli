# Pueblo CLI

Pueblo CLI is a notarized macOS command-line companion for the Pueblo app. It is distributed separately from the private Pueblo app source repository.

**[Download Pueblo CLI 0.3.1](https://github.com/ShawnCrawford/pueblo-cli/releases/latest/download/pueblo-cli-0.3.1-macos-universal.zip)** · [Installation guide](INSTALL.md)

The universal package supports Apple silicon and Intel Macs. Pueblo must be open and **CLI Access** enabled for commands to connect. The CLI sends authenticated requests to Pueblo's local service; it does not open the app's database or connect to CloudKit directly.

Pueblo CLI 0.3.1 can list and search clients, contacts, leads, engagements, and journal entries; show record details; create or edit supported records; and manage checklist items with `pueblo todo list|add|update|complete|reopen|delete`. Pairing reads the code without terminal echo, including with the signed sandboxed CLI. Deleting a checklist item deletes only that item. Leads remain read-only, and deleting CRM records is unsupported.

**Compatibility:** Checklist commands require a Pueblo macOS app build that includes the checklist CLI service. Earlier app builds continue to support their existing CLI operations and return `feature_unavailable` for checklist commands. Update Pueblo before using `pueblo todo`.

See `pueblo help --ai` for command syntax and local AI-agent guidance. Review the [release notes](https://github.com/ShawnCrawford/pueblo-cli/releases) and verify the downloaded ZIP with `SHA256SUMS` before installation.
