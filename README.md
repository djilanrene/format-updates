# Format — Professional Document Editor

**Format** is a desktop application for creating professional documents — quotes, invoices, estimates — without relying on cloud services or internet connectivity. Your data stays on your machine.

> This repository hosts public releases and powers the in-app auto-update system.

---

## Download

**[⬇ Download latest version](https://github.com/djilanrene/format-updates/releases/latest)**

| Platform | Installer |
|----------|-----------|
| Windows 10/11 (x64) | `format-setup-vX.X.X.exe` |

---

## Features

- Create quotes, invoices and professional documents from built-in templates
- Fill structured forms — client info, line items, taxes, payment terms
- Live preview with pagination, PDF and HTML export
- Personal template system — import custom `.json` or `.zip` templates
- Dark/light theme, custom accent color, typography settings
- Fully offline — no account, no cloud, no telemetry
- Auto-update notifications via this repository

---

## Installation

See [docs/INSTALLATION.md](docs/INSTALLATION.md) for a step-by-step guide.

**Quick start:**
1. Download `format-setup-vX.X.X.exe` from the [latest release](https://github.com/djilanrene/format-updates/releases/latest)
2. Run the installer (click "Run anyway" if Windows SmartScreen appears — see [FAQ](#smartscreen))
3. Launch Format from the Start menu or Desktop shortcut

---

## Updating

Format checks for updates automatically at startup. When a new version is available, a badge appears in the settings panel.

You can also check manually: **Settings → Updates → Check now**

See [docs/UPDATE.md](docs/UPDATE.md) for details.

---

## FAQ

### SmartScreen warning on first install {#smartscreen}

Windows Defender SmartScreen may block the installer with a message like *"Windows protected your PC"*. This happens because the app is not yet code-signed.

**It is safe to proceed:** click **"More info" → "Run anyway"**.

This warning disappears automatically as the installer accumulates download reputation.

### Where is my data stored?

All your documents and settings are stored locally:

| Data | Location |
|------|----------|
| Documents (`.fmt`) | Wherever you save them |
| Settings | `%APPDATA%\format-desktop\` |
| Personal templates | `Documents\Format\Templates\` |

Nothing is sent to any server.

### Can I use Format on multiple machines?

Yes. Copy your `.fmt` files between machines — they are self-contained JSON files. For settings and templates, copy the folders listed above.

---

## Reporting a bug

Use the [Bug report](https://github.com/djilanrene/format-updates/issues/new?template=bug_report.md) issue template.

Please include your Format version (visible in **Settings → About**) and your Windows version.

---

## Security

To report a security vulnerability, see [SECURITY.md](SECURITY.md). Do not open a public issue for security matters.

---

## About

Format is developed and maintained by **Pluton Projects**.

© 2026 Pluton Projects — All rights reserved. Proprietary software — personal use only.
