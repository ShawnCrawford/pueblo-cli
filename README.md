# Pueblo CLI

Pueblo CLI is a notarized macOS command-line companion for the Pueblo app. It is distributed separately from the Pueblo app source repository.

**[Download Pueblo CLI 0.1.0](https://github.com/ShawnCrawford/pueblo-cli/releases/latest/download/pueblo-cli-0.1.0-macos-universal.zip)** · [Installation guide](INSTALL.md)

The universal package supports Apple silicon and Intel Macs. Pueblo must be open and **CLI Access** enabled for commands to connect. The CLI sends authenticated requests to Pueblo's local service; it does not open the app's database or connect to CloudKit directly.

It can list and search clients, contacts, engagements, and journal entries, show record details, and create journal entries. Journal creation is the only write. It cannot edit or delete records, and `todo list` is unavailable.

See `pueblo help --ai` for command syntax and local AI-agent guidance. Review the [release notes](https://github.com/ShawnCrawford/pueblo-cli/releases) and verify the downloaded ZIP with `SHA256SUMS` before installation.
