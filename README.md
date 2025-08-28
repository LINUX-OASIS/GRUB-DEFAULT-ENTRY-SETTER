# 🚀 GRUB Default Setter 🚀

![Language](https://img.shields.io/badge/language-Bash-4EAA25.svg?style=for-the-badge)
![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg?style=for-the-badge)
![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=for-the-badge)
![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-green.svg?style=for-the-badge)

A user-friendly, TUI-based shell script to safely and easily set the default boot entry for the GRUB bootloader. Say goodbye to manually editing configuration files and risking boot errors!

---

## ✨ Features

*   **Interactive TUI:** A clean `whiptail` interface guides you through the process. No more error-prone manual editing of `/etc/default/grub`!
*   **Automatic Entry Detection:** The script intelligently parses your `/boot/grub/grub.cfg` to find all available top-level and sub-menu boot entries.
*   **Safety First:**
    *   Automatically requests root permissions via `sudo`.
    *   Verifies required dependencies before running.
    *   Creates a backup of your configuration (`/etc/default/grub.bak`) before making any changes.
    *   Requires a final confirmation before applying settings and running `update-grub`.
*   **Flexible Formatting:** Lets you choose the GRUB entry format that works best for your system's configuration.
*   **Aesthetic Theming:** Includes a custom color scheme for `whiptail` to provide a more visually appealing experience.

## 🖥️ Compatibility

This script is designed for Linux distributions that use the GRUB2 bootloader, the `apt` package manager, and the `update-grub` command. It is tested and confirmed to work with:

[!Ubuntu](https://ubuntu.com/)
[!Debian](https://www.debian.org/)
[!Linux Mint](https://linuxmint.com/)

It should also work on most derivatives of Debian and Ubuntu.

## 🛠️ Dependencies

The script relies on a few common tools to function correctly:

*   `bash` (v4.0 or newer for associative arrays)
*   `whiptail` (provides the TUI dialog boxes)
*   `sudo` (for administrative privileges)
*   Standard GNU core utilities (`grep`, `sed`, `awk`).

The script includes pre-flight checks to ensure a safe run:
*   **Root Privileges:** It will automatically re-launch itself with `sudo` if you forget to run it as root.
*   **Whiptail Dependency:** It checks if `whiptail` is installed. If not, it will abort and **provide you with the exact command** to install it on your system.

## ⚙️ Installation & Usage

1.  Clone the repository or download the `custom-GRUB-DEFAULT-SETTER.sh` script.
    ```bash
    # Example using git
    git clone https://github.com/LINUX-OASIS/GRUB-DEFAULT-ENTRY-SETTER.git
    cd GRUB-DEFAULT-ENTRY-SETTER
    ```

2.  Make the script executable.
    ```bash
    chmod +x custom-GRUB-DEFAULT-SETTER.sh
    ```

3.  Run the script.
    ```bash
    ./custom-GRUB-DEFAULT-SETTER.sh
    ```

4.  Follow the on-screen TUI instructions to select your desired default boot entry, confirm your choice, and let the script handle the rest!

## 💬 Contributing

Pull requests, issues, and suggestions are warmly welcomed!

For major changes, please open an issue first to discuss what you would like to change. See CONTRIBUTING.md for development guidelines.

## 🌐 Links

*   Report an Issue
*   Open a Pull Request
*   View Releases
*   Project Wiki

## 🧙‍♂️ Maintainer

*   **LINUX-OASIS**

## 📜 License

This project is licensed under the GNU General Public License v3.0. See the LICENSE file for details.

```
Copyright (C) 2024 LINUX-OASIS

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <https://www.gnu.org/licenses/>.
```
