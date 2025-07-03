# Windows Recovery USB with Custom Menu
Custom WinPE USB to reset passwords, fix accounts, and recover access.
![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)

This project lets you create a bootable Windows PE (WinPE) USB stick with a custom recovery menu for:
- Resetting Windows passwords
- Replacing/restoring utilman.exe
- Enabling admin accounts
- Rebooting into Safe Mode

## 🔧 Requirements

- Windows 10 or 11
- [Windows ADK](https://learn.microsoft.com/en-us/windows-hardware/get-started/adk-install) (Deployment Tools only)
- [WinPE Add-on for ADK](https://learn.microsoft.com/en-us/windows-hardware/manufacture/desktop/winpe-add-on-install)
- USB stick (≥ 1 GB, will be formatted)

## 🚀 Quick Start

1. Clone the repo:
    ```bash
    git clone https://github.com/sygoras/WinPE-Recovery-USB.git
    ```

2. Open **Deployment and Imaging Tools Environment** as Administrator:
   - Found in Start → Windows Kits
   - Right-click → Run as Administrator

3. Run the builder script:
    ```cmd
    cd WinPE-Recovery-USB
    BuildRecoveryUSB.bat
    ```

4. Select your USB drive (default: E:)

5. Boot from the USB to use the recovery menu!

## 📜 Menu Functions

- **1**: Replace `utilman.exe` with `cmd.exe` (login screen CMD trick)
- **2**: Restore original `utilman.exe` from backup
- **3**: Enable built-in Administrator + set password
- **4**: Create new local Administrator user
- **5**: Show detailed system info
- **6**: Reboot into Safe Mode
- **7**: Reboot now
- **Esc**: Exit to Command Prompt

## 🛑 Disclaimer

This tool is for recovery and educational use only. Do not use on machines without proper authorization.

## 📝 License

This project is licensed under the [MIT License](LICENSE) © Tomas Sprogys (sygoras).  
You are free to use, modify, and distribute this software with attribution and at your own risk.
