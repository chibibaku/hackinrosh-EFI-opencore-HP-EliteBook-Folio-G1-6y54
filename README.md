# About
## Hardware
## Software
- macOS 14 Sonoma (14.1.2)
- OpenCore 0.9.6
- Working very well as MacBook9,1
### Note
kexts are up-to-date in Dec. 9th 2023.\
AirportItlwm using v2.3.0 alpha which experimental support for sonoma.\
# Installation
Follow dortania OpenCore guide.\
Copy downloaded EFI folder to EFI partition.\
Setup *your* SMBIOS (serial, MLB, etc...) with GenSMBIOS.
**Model: `MacBook9,1`**

Then, follow the note down below and change the model as iMacPro1,1 once.
## Important note
Once you create flash drive, you need to change the model as iMacPro1,1 in first installer boot.

After the first reboot which "macOS Installer" has appeare, Turn off your device and disconnect USB flash drive and change back your model to MacBook9,1. This is because of to avoid the message "macOS Sonoma is not compatible with this mac". MacBook9,1 is not officaly supported model for macOS Sonoma.

Model propatie at: `SMBIOS > Generic > SystemProductName`
# Status
## Verified supported OS
- macOS 14 Sonoma (14.1.2)
## What works
- CPU
  - iGPU (spoof to KabyLake iGPU)
  - Clock management
- Integrated Speaker / Mic
- Keyboard
  - Brightness / Sound sdjustment keys
- Trackpad *1
- WiFi / BT
- Battery status
- Sleep / wake
- USB-C

*1 Known issue : Cursor suddenly warp when touch edge of trackpad.
## What *NOT* works
- Thunderbolt 3 (work as USB-C)
- 3.5mm Audio