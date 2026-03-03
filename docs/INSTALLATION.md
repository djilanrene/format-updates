# Installation Guide

## System requirements

| | Minimum |
|-|---------|
| OS | Windows 10 (64-bit) |
| RAM | 4 GB |
| Disk | 300 MB |
| Display | 1280 × 720 |

---

## Step-by-step installation

### 1. Download the installer

Go to the [latest release](https://github.com/djilanrene/format-updates/releases/latest) and download `format-setup-vX.X.X.exe`.

---

### 2. Handle the SmartScreen warning

When you run the installer, Windows Defender SmartScreen may show:

> **"Windows protected your PC"**
> Microsoft Defender SmartScreen prevented an unrecognized app from starting.

This is expected for apps that are not yet code-signed by a recognized publisher.

**To proceed:**
1. Click **"More info"**
2. Click **"Run anyway"**

This warning will disappear as the app accumulates download reputation with Microsoft.

---

### 3. Accept the license

Read and accept the End User License Agreement to continue.

---

### 4. Choose installation directory

The default location is:
```
C:\Users\<you>\AppData\Local\Programs\Format
```

You can change this. The app does not require administrator rights if you install to your user directory.

---

### 5. Create shortcuts

By default the installer creates:
- A **Desktop shortcut**
- A **Start menu entry**

Both are optional and can be unchecked.

---

### 6. Launch Format

Click **Finish** to launch Format immediately, or find it in the Start menu under **Format**.

On first launch, a short setup wizard will guide you through:
- Choosing your default document folder
- Setting up a personal templates folder
- Configuring update preferences

---

## After installation

### File association

Format registers the `.fmt` extension. Double-clicking a `.fmt` file will open it directly in Format.

### Personal templates folder

A folder is created automatically at:
```
Documents\Format\Templates\
```

Drop your custom template files here. They will appear in the **PERSONAL** tab of the template gallery on next launch.

---

## Silent / unattended installation

The installer supports silent mode for IT deployment:

```cmd
format-setup-vX.X.X.exe /S
```

To specify a custom install directory:

```cmd
format-setup-vX.X.X.exe /S /D=D:\Apps\Format
```

---

## Troubleshooting installation

See [TROUBLESHOOTING.md](TROUBLESHOOTING.md) for common issues.
