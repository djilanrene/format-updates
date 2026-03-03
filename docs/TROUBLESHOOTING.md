# Troubleshooting

---

## Installation issues

### "Windows protected your PC" (SmartScreen)

**Symptom:** A warning dialog appears when running the installer.

**Cause:** The installer is not yet code-signed by a recognized publisher. This is a reputation-based warning, not an indication of malware.

**Fix:**
1. Click **"More info"**
2. Click **"Run anyway"**

---

### Installer fails silently or closes immediately

**Possible causes:**
- Antivirus blocking the installer
- Insufficient disk space (need ~300 MB)
- Corrupted download

**Fix:**
1. Temporarily disable real-time antivirus protection
2. Re-download the installer and verify the file size matches the release
3. Run as administrator if installing to a system directory

---

### App does not appear after installation

**Fix:**
- Check the Start menu: search for **Format**
- Check the install directory: `%LOCALAPPDATA%\Programs\Format\Format.exe`
- Re-run the installer — it is safe to install over an existing installation

---

## Launch issues

### App opens and immediately closes

**Possible cause:** Corrupted configuration file.

**Fix:**
1. Open `%APPDATA%\format-desktop\`
2. Delete or rename `config.json`
3. Relaunch Format — the first-launch wizard will reappear

---

### Blank white screen on launch

**Possible cause:** GPU rendering issue with Electron on some hardware configurations.

**Fix:** Launch with hardware acceleration disabled:
```cmd
"C:\Users\<you>\AppData\Local\Programs\Format\Format.exe" --disable-gpu
```

---

### First-launch wizard loops or never ends

**Cause:** `config.json` was written but is malformed.

**Fix:**
1. Close Format
2. Delete `%APPDATA%\format-desktop\config.json`
3. Relaunch

---

## Document issues

### A `.fmt` file does not open with double-click

**Cause:** File association was not registered, or was overwritten by another app.

**Fix:**
1. Right-click the `.fmt` file
2. Select **"Open with"** → **"Choose another app"**
3. Find `Format.exe` at `%LOCALAPPDATA%\Programs\Format\`
4. Check **"Always use this app"**

---

### Preview does not refresh after editing

**Fix:** Press **F5** (switch to preview) or **F6** (toggle preview panel). The preview renders on demand, not in real time.

---

### PDF export has unwanted margins

The PDF export uses your browser's print dialog. To remove margins:

1. Press **Ctrl+P** to open the print dialog in the preview
2. Click **More settings**
3. Set **Margins** to **None**
4. Select **Save as PDF**

---

## Update issues

### "Check now" shows no update even though a new version exists

**Possible causes:**
- Network request blocked by a firewall or proxy
- GitHub Pages cache not yet propagated

**Fix:** Wait a few minutes and try again. If the issue persists, download the latest version manually from the [releases page](https://github.com/djilanrene/format-updates/releases).

---

### Update badge appears but download link does not open

**Fix:** Make sure a default browser is set in Windows. The download button opens your browser to the GitHub release page.

---

## Templates issues

### Personal templates do not appear in the gallery

**Possible causes:**
- Templates are not in the correct folder
- Template file has a syntax error

**Fix:**
1. Check the templates folder path in **Settings → Locations → Personal templates**
2. Make sure your template is a valid `.json` or `.zip` file
3. Restart Format — templates are scanned on startup

---

## Still stuck?

Open a [bug report](https://github.com/djilanrene/format-updates/issues/new?template=bug_report.md) and include:
- Your Format version (**Settings → About**)
- Your Windows version
- Steps to reproduce the issue
- Any error message visible on screen
