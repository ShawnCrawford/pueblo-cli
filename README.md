# Pueblo CLI

Pueblo CLI is a notarized macOS command-line companion for the Pueblo app. It is distributed separately from the private Pueblo app source repository.

**[Download Pueblo CLI 0.4.0](https://github.com/ShawnCrawford/pueblo-cli/releases/latest/download/pueblo-cli-0.4.0-macos-universal.zip)** · [Installation guide](INSTALL.md)

The universal package supports Apple silicon and Intel Macs. Pueblo must be open and **CLI Access** enabled for commands to connect. The CLI sends authenticated requests to Pueblo's local service; it does not open the app's database or connect to CloudKit directly.

Pueblo CLI 0.4.0 can list, search, and show clients, contacts, leads, engagements, and journal entries; create and edit supported records, including leads; manage checklist items; apply bounded mixed-record edits with a dry-run preview; and delete CRM entities by explicit UUID after preview and user authorization. Pairing reads the code without terminal echo, including with the signed sandboxed CLI. Checklist deletion applies to one checklist item UUID.

**Compatibility:** Checklist commands and the 0.4.0 Lead, batch-edit, and entity-delete operations require a Pueblo macOS app build that includes the matching CLI services. Earlier app builds continue to support existing CLI operations and return `feature_unavailable` for unsupported commands. Update Pueblo before using these newer operations.

See `pueblo help --ai` for command syntax and local AI-agent guidance. Review the [release notes](https://github.com/ShawnCrawford/pueblo-cli/releases) and verify the downloaded ZIP with `SHA256SUMS` before installation.
