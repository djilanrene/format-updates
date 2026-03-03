# Uninstalling Format

## Standard uninstall

1. Open **Windows Settings** → **Apps** (or **Control Panel → Programs**)
2. Find **Format** in the list
3. Click **Uninstall** and follow the prompts

This removes the application files and Start menu/Desktop shortcuts.

---

## What the uninstaller does NOT remove

The uninstaller only removes the application itself. The following are left untouched to preserve your data:

| What | Location |
|------|----------|
| App settings | `%APPDATA%\format-desktop\` |
| Personal templates | `Documents\Format\Templates\` |
| Your documents (`.fmt` files) | Wherever you saved them |

---

## Complete removal (all data)

If you want to remove everything:

1. Uninstall via Windows Settings (step above)
2. Delete the settings folder:
   ```
   %APPDATA%\format-desktop\
   ```
3. Delete the personal templates folder:
   ```
   Documents\Format\Templates\
   ```
4. Delete any `.fmt` documents you no longer need

### Remove the file association

To remove the `.fmt` file association from Windows:

1. Open **Registry Editor** (`regedit`)
2. Navigate to `HKEY_CLASSES_ROOT\.fmt`
3. Delete the key

Or use a third-party tool like **File Types Manager** to do this without touching the registry manually.

---

## Reinstalling after a full removal

After a complete removal, reinstalling Format will trigger the first-launch wizard again, as if it were a fresh install.
