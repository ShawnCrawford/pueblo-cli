# Install Pueblo CLI

1. Download `pueblo-cli-0.2.0-macos-universal.zip` and `SHA256SUMS` from the [latest release](https://github.com/ShawnCrawford/pueblo-cli/releases/latest). The package supports Apple silicon and Intel Macs.
2. In Terminal, go to the folder containing both downloads and verify the ZIP:

   ```sh
   shasum -a 256 -c SHA256SUMS
   ```

   The result should say `OK`.

3. Extract the ZIP and run its per-user installer:

   ```sh
   unzip pueblo-cli-0.2.0-macos-universal.zip
   cd PuebloCLI-0.2.0
   ./install.sh
   ```

   The installer verifies the bundle signature and entitlements, installs the complete app-like bundle under `~/Library/Application Support/PuebloCLI/`, and links `pueblo` from `~/.local/bin/`. It does not require administrator access or edit shell startup files. It stops without replacing another command already at `~/.local/bin/pueblo`.

4. If Terminal cannot find `pueblo`, add this line to `~/.zprofile`, then open a new Terminal window:

   ```sh
   export PATH="$HOME/.local/bin:$PATH"
   ```

5. Open Pueblo, enable **CLI Access**, and generate a pairing code. In Terminal, run `pueblo pair` and enter the code when prompted. The code expires after five minutes and is not echoed. Confirm the connection with `pueblo status`.

Pueblo must remain open while you use the CLI. Revoke **CLI Access** in Pueblo to stop future requests. Run `pueblo unpair` to remove the CLI's saved credential.

## Upgrade and removal

Run `./install.sh --rollback` from the extracted package folder to restore the previous installed bundle. Run `./uninstall.sh` to move the active bundle aside and remove the command link. These operations do not delete credentials or change Pueblo records. To fully revoke access, revoke **CLI Access** in Pueblo; run `pueblo unpair` before uninstall if you also want to remove the CLI's Keychain credential.

## Supported commands and data boundary

Pueblo CLI sends authenticated requests to the open Pueblo app. It does not access SwiftData or CloudKit directly. Version 0.2.0 supports list, search, and detail reads for clients, contacts, leads, engagements, and journal entries. It supports create and edit for clients, contacts, engagements, and journal user notes. Leads are read-only. There is no delete operation, and `todo list` is unavailable.

The new create/edit commands require a compatible Pueblo macOS app release containing the 0.2.0 service protocol. Until then, existing supported CLI commands remain available and newer operations may be rejected as unavailable. Pueblo remains responsible for field validation and relationship integrity. Only the running app writes its own store.
