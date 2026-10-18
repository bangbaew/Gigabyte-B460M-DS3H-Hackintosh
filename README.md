# Gigabyte B460M DS3H Hackintosh

OpenCore EFI for the **Gigabyte B460M DS3H** (Comet Lake). Updated to current OpenCore/kexts.

## Hardware
- **CPU:** Intel Core i5-10400 / i7-10700 (Comet Lake)
- **RAM:** Kingston HyperX Fury 16GB DDR4 + Kingston HyperX Predator RGB 16GB DDR4 @ 2666 MHz
- **Motherboard:** Gigabyte B460M DS3H (BIOS F5d or newer)
- **GPU:** XFX Radeon RX 480 4GB (primary) + Intel UHD Graphics 630 (now ASUS TUF Gaming Radeon RX 6900 XT)
- **SSD:** Transcend MTE220S M.2 NVMe 512GB (TS512GMTE220S)
- **Audio:** Realtek ALC887
- **Network:** Realtek RTL8111 (onboard) + DW1820A CN-096JNT (BCM94350ZAE) Wi-Fi/BT (now Fenvi FV-T919 BCM94360CD)
- **Bootloader:** OpenCore 1.0.5
- **SMBIOS:** iMac20,1
- **Target macOS:** Sonoma (14) and newer (Sequoia 15 supported, kernel >= 23.x)

## Important
**Please change your SMBIOS serial number / MLB / ROM after installing this EFI folder.** Do not use the serials shipped in the config.

## What's working
- Onboard Audio ALC887 (layout-id = 5)
- USB 3.0
- Sleep / Wake
- Wi-Fi (Sonoma+ path via IOSkywalkFamily + IO80211FamilyLegacy)
- Bluetooth
- AirDrop, Handoff & Universal Clipboard
- iMessage & other iServices
- iGPU acceleration (SMBIOS iMac20,1)
- Full RX 480 hardware acceleration (`agdpmod=pikera`)
- Dual boot Windows from OpenCore (disable DSDT.aml)

## Known issues / Not working
- DW1820A cannot see 5 GHz Wi-Fi on channel 36 (Solved by Fenvi FV-T919)
- Using HDMI on the iGPU (Intel UHD 630) gives a black screen

## Included kexts
| Kext | Version |
| --- | --- |
| Lilu | 1.7.1 |
| VirtualSMC | 1.3.7 |
| WhateverGreen | 1.7.0 |
| AppleALC | 1.9.6 |
| NVMeFix | 1.1.0 |
| RealtekRTL8111 | 3.0.0 |
| USBInjectAll | 0.8.1 |
| XHCI-unsupported | 0.9.2 |
| VoodooPS2Controller | 2.3.7 |
| AirportBrcmFixup | 2.2.0 |
| BrcmPatchRAM3 | 2.5.9 |
| BrcmBluetoothInjector | 2.6.0 |
| IOSkywalkFamily | 1.0 |
| IO80211FamilyLegacy | 12.0 |
| AMFIPass | 1.4.1 |
| CtlnaAHCIPort | 341.0.2 |

## Notes
- Broadcom Wi-Fi on Sonoma/Sequoia uses `IOSkywalkFamily` + `IO80211FamilyLegacy` + `AMFIPass` (boot-arg `amfi=0x80`).
- Audio uses `layout-id = 5`.
- For dual-booting Windows, disable `DSDT.aml` as needed.