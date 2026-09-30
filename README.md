# Pueblo CLI

Pueblo CLI is a notarized macOS command-line companion for the Pueblo app. It is distributed separately from the private Pueblo app source repository.

**[Download Pueblo CLI 0.2.0](https://github.com/ShawnCrawford/pueblo-cli/releases/latest/download/pueblo-cli-0.2.0-macos-universal.zip)** · [Installation guide](INSTALL.md)

The universal package supports Apple silicon and Intel Macs. Pueblo must be open and **CLI Access** enabled for commands to connect. The CLI sends authenticated requests to Pueblo's local service; it does not open the app's database or connect to CloudKit directly.

Pueblo CLI 0.2.0 can list and search clients, contacts, leads, engagements, and journal entries; show record details; and create or edit clients, contacts, engagements, and journal user notes. Leads are read-only. Deleting records and `todo list` are unsupported.

**Compatibility:** the new create/edit commands require a Pueblo macOS app release that includes the 0.2.0 CLI service protocol. Until that compatible app release is available, the installed CLI's existing supported commands continue to work and newer operations may be rejected as unavailable.

See `pueblo help --ai` for command syntax and local AI-agent guidance. Review the [release notes](https://github.com/ShawnCrawford/pueblo-cli/releases) and verify the downloaded ZIP with `SHA256SUMS` before installation.
