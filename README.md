# About
## Hardware

## Software
- macOS 14 Sonoma (14.1.2)
- OpenCore 0.9.6
- SMBIOS: MacBook9,1

### Note
- Kexts updated: December 9th, 2023
- AirportItlwm: v2.3.0 alpha (experimental Sonoma support)
- To use this configuration, ensure OC, kexts, and necessary files are updated to the latest versions

# Installation
Follow Dortania's OpenCore guide as a general rule.

1. Copy the EFI folder to your EFI partition
2. Setup your SMBIOS (serial, MLB, etc.) with GenSMBIOS using `MacBook9,1` model

**Note**: macOS Sonoma installer will refuse to install with MacBook9,1 model as it's not officially supported. You'll need to temporarily use iMacPro1,1 during installation to avoid the "macOS Sonoma is not compatible with this Mac" message.

## Installation Steps

1. Change the model to `iMacPro1,1` in `SMBIOS > Generic > SystemProductName`
   - No need to change serial or MLB values
2. Boot with the installer USB flash drive
3. Format the internal drive
4. Start the installation
5. After the first reboot when "macOS Installer" appears in the boot picker:
   1. Turn off your device
   2. Disconnect the installer drive
   3. Connect installer drive to a host computer
   4. Change the model back to `MacBook9,1`
   5. Reconnect installer drive to the laptop
6. Boot into picker
7. Select "macOS Installer" and continue with installation

# Status
## Verified supported OS
- macOS 14 Sonoma (14.1.2)

## What works
- CPU
  - iGPU (spoofed to KabyLake iGPU)
  - Clock management
- Integrated Speaker / Mic
- Keyboard
  - Brightness / Sound adjustment keys
- Trackpad*
- WiFi / BT
- Battery status
- Sleep / wake
- USB-C

*Known issue: Cursor may suddenly warp when touching the edge of trackpad

## What does NOT work
- Thunderbolt 3 (works only as USB-C)
- 3.5mm Audio jack