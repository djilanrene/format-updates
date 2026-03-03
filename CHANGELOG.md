# Changelog — Format

All notable changes visible to users are documented here.
For the full technical changelog, see the [private repository](https://github.com/djilanrene/format).

---

## [0.5.0] — 2026-03-03

### What's new
- Your personal templates folder (`Documents\Format\Templates`) is now created automatically on first launch — no need to create it manually

### Improvements
- Release notes now show a descriptive title summarizing what changed

---

## [0.4.0] — 2026-03-03

### What's new
- The fullscreen button now shows **"Restore screen"** when in fullscreen mode, and switches back to **"Fullscreen"** when exiting — with matching icons

### Fixed
- Brief flash of the empty screen when closing the application
- App icon was missing in the titlebar and settings panel after installation
- License text displayed garbled characters in the installer window
- Duplicate "Check for updates" button removed from the settings panel
- Unnecessary "Read only" label removed from the native templates row in settings

### Changes
- App rebranded to **Pluton Projects**
- Installer file renamed to `format-setup-vX.X.X.exe` (lowercase, with version prefix)

---

## [0.3.0] — 2026-03-03

### What's new
- **Focus mode** (Ctrl+F11): hides all interface chrome — only the document canvas remains
- **Fullscreen** (F11): hides the titlebar while keeping the ribbon and editor
- Press **Escape** to exit focus mode
- Dedicated fullscreen button in the AFFICHAGE ribbon tab
- Click the page format in the status bar for a quick-select popover
- **Custom page size** option in layout settings (free width/height)
- **Automatic system font detection** in Typography settings
- **Automatic text color adaptation** based on accent color brightness (WCAG 2.1)
- **Import personal templates**: supports `.json` and `.zip` files
- **Locations section** in settings: manage your personal templates folder
- Personal templates step added to the first-launch wizard
- **PERSONAL tab** in the template gallery with an Import button

### Fixed
- Opening a template required 2 clicks to display the editor
- Double tab created when clicking a template
- Recent files did not open on click
- About section was empty on first open in settings
- Dark theme applied but dropdown showed "Clair"
- Titlebar showed the last document name with no document open
- Action buttons visible in file menu with no document open

---

## [0.2.0] — 2026-03-02

### What's new
- Live document preview with pagination
- Declarative template system — templates can now be written as simple JSON files
- Automatic template loading — new templates appear without editing any app file

---

## [0.1.0] — 2026-02-28

### What's new
- Initial release
- Create professional documents from the built-in **Devis standard** template
- Structured form: client info, line items, taxes, payment terms, notes, signature
- PDF and HTML export
- Dark/light theme with custom accent color
- Auto-save, undo/redo, dirty indicator
- Multi-tab document management
- Settings panel: typography, layout, appearance, locations, updates
- Auto-update check on startup
