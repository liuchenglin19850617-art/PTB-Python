# [Project Name]

[![License: LGPL v3](https://img.shields.io/badge/License-LGPL--3.0-blue.svg)](LICENSE)
[![Platform: Windows](https://img.shields.io/badge/Platform-Windows-lightgrey.svg)]()
[![Python 3.x](https://img.shields.io/badge/Python-3.x-yellow.svg)](https://www.python.org/)

[Project Name] is a portable, open-source Windows application built on Python. It bundles the Python runtime and required dependencies, so **no installation is required** — just extract and run. It does not modify the registry or rely on a system-wide Python installation. Optional administrator elevation is supported for tools that need elevated privileges.

The source code is released under the **GNU Lesser General Public License v3.0 (LGPL-3.0)**. This distribution also includes the Python Software Foundation License Version 2 and other third-party licenses. See the [`licenses/`](licenses/) directory for details.

---

## Features

- **Portable** — Extract to any folder and run. Can be placed on a USB drive, external hard drive, or cloud-synced folder.
- **No installation** — No need to install Python beforehand. No registry writes, no system pollution.
- **Bundled runtime** — Includes the Python interpreter and required third-party libraries.
- **Optional administrator elevation** — Can request administrator privileges when needed.
- **Open source** — Source code released under LGPL-3.0. Contributions are welcome.
- **License compliant** — Retains the Python license and all third-party licenses and copyright notices.

---

## System Requirements

- Windows 10 / 11 (64-bit)
- No Python installation required
- If administrator privileges are needed, a UAC prompt will appear at startup

---

## Download

Go to the [Releases](https://github.com/[your-username]/[Project Name]/releases) page and download the latest package:

- `[Project Name]-vX.Y.Z-win64.zip`

Extract it to any folder and you are ready to go.

---

## Quick Start

1. Download and extract `[Project Name]-vX.Y.Z-win64.zip`.
2. Double-click `run.bat` or `[Project Name].exe` to start the application.
3. If administrator privileges are required, right-click and select **Run as administrator**, or simply double-click (if built with `--uac-admin`, it will request elevation automatically).

> The application does not write to system directories or the registry. All configuration is stored in `config.json` inside the application folder.

---

## Building from Source

### Option 1: Using the Embedded Python Package (recommended for portable builds)

1. Download the official [Windows embeddable package (64-bit)](https://www.python.org/downloads/windows/).
2. Extract it into the `python/` directory.
3. Edit `python/python3xx._pth` to include your application path and `site-packages`:

   ```text
   python3xx.zip
   .
   ..\app
   ..\Lib\site-packages
   import site
