# Update System

## How it works

Format checks for updates by fetching a small JSON file hosted on GitHub Pages:

```
https://djilanrene.github.io/format-updates/version.json
```

This file contains the latest version number, release date, changelog summary, and download URL. No personal data is sent — it is a simple HTTPS GET request.

### version.json structure

```json
{
  "version": "0.5.0",
  "date": "2026-03-03",
  "notes": "...",
  "download": "https://github.com/djilanrene/format-updates/releases/download/v0.5.0/format-setup-v0.5.0.exe"
}
```

### Update check flow

```
App starts
    │
    ▼
Fetch version.json  ──── network error? ──▶ silently skip
    │
    ▼
Compare with installed version (semver)
    │
    ├── up to date ──▶ nothing shown
    │
    └── new version available
            │
            ▼
        Badge on Settings icon
        Banner in Settings → Updates
        "Download" button → opens browser
```

The app never downloads or installs anything automatically. You always control when and whether to update.

---

## Automatic check at startup

Enabled by default. Can be disabled in **Settings → Updates → Check automatically on startup**.

When disabled, you can still check manually at any time.

---

## Manual check

1. Open **Settings** (bottom-left)
2. Scroll to **Updates**
3. Click **Check now**

---

## Installing an update

Format does not auto-install updates. When a new version is available:

1. Click **Download** in the update banner — your browser opens the release page
2. Download `format-setup-vX.X.X.exe`
3. Run the installer over the existing installation

**Your documents and settings are preserved.** The installer updates the application files only.

---

## Disabling updates entirely

Go to **Settings → Updates** and uncheck **Check automatically on startup**.

You can still download new versions manually from the [releases page](https://github.com/djilanrene/format-updates/releases) at any time.
