# Security Policy

## Supported versions

Only the latest release receives security fixes.

| Version | Supported |
|---------|-----------|
| Latest  | ✅ |
| Older   | ❌ |

## Reporting a vulnerability

**Do not open a public GitHub issue for security vulnerabilities.**

Send a private report to: **contact@plutonprojects.com**

Please include:
- A description of the vulnerability
- Steps to reproduce
- Potential impact
- Your Format version (visible in **Settings → About**)

You will receive a response within 7 days. If the issue is confirmed, a fix will be released as soon as possible and you will be credited in the release notes (unless you prefer to remain anonymous).

## Scope

Format is a local desktop application. It does not run a server, does not expose network ports, and does not transmit user data. The primary attack surface is:

- The Electron/Chromium renderer process
- File parsing (`.fmt` documents, template `.json`/`.zip` imports)
- The auto-update URL fetch (`version.json` over HTTPS)

Reports in these areas are most relevant.
