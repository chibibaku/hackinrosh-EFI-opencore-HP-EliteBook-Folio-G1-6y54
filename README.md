# About
## Hardware
## Software
- macOS 14 Sonoma (14.1.2)
- OpenCore 0.9.6
- Working very well as MacBook9,1
### Note
The kexts are updated as latest version in Dec. 9th 2023.\
AirportItlwm using v2.3.0 alpha which experimental support for sonoma.\
In order to use, please update OC, Kext, and necessary files to the latest.\
# Installation
As a general rule, follow dortania's OpenCore guide.\
Copy downloaded EFI folder to EFI partition.\
Setup *your* SMBIOS (serial, MLB, etc...) with GenSMBIOS.
**Model: `MacBook9,1`**

However, The installer will refuse to install Sonoma with `MacBook9,1` model.
This is because of this model is not officaly supported in macOS Sonoma.
So keep following the instruction down below and change the model as `iMacPro1,1` while install.
Otherwise, you'll get "macOS Sonoma is not compatible with this mac" message and cannot go further.

## Important note
While booting the installer, you need to change the model as `iMacPro1,1`.
Model propatie at: `SMBIOS > Generic > SystemProductName`

1. Change the model model as `iMacPro1,1`.
  - You don't need to mind about serial or MLB.
2. Boot with installer USB flash drive.
3. Format the internal drive.
4. Start the installation.
5. After the first reboot and while in the boot picker with "macOS Installer" has appeared:
   1. Turn off your device
   2. Disconnect the installer drive
   3. Plug installer drive into host computer
   4. Write back the model to `MacBook9,1`
6. Plug installer drive back to laptop.
7. Boot into picker
8. Select "macOS Installer" and leave it while installation.

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