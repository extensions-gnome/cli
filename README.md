# GNOME Extension Store CLI Helper

A lightweight Python CLI tool to install, update, and manage GNOME Shell extensions directly from the terminal or through web integration.

## Installation & Setup

You can download and register the helper (integrating it with the web catalog for one-click installs and setting up hourly background updates) using this command:

```bash
curl -sSL https://raw.githubusercontent.com/extensions-gnome/store/main/gnome-ext-cli -o /tmp/gnome-ext-cli && chmod +x /tmp/gnome-ext-cli && /tmp/gnome-ext-cli register && /tmp/gnome-ext-cli setup-autoupdate && rm /tmp/gnome-ext-cli
```

## CLI Commands

* `gnome-ext-cli register`: Installs the CLI in `~/.local/bin/` and registers the `gnome-ext://` protocol handler.
* `gnome-ext-cli setup-autoupdate`: Configures an hourly background systemd timer to automatically check for and install updates.
* `gnome-ext-cli check-updates`: Scans installed extensions and compares their versions with the store database.
* `gnome-ext-cli update --all`: Downloads and updates all outdated extensions from the store database.
* `gnome-ext-cli install <uuid>`: Downloads and installs an extension by its UUID.
