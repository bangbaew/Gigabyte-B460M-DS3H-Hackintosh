My Build
- OS: macOS Big Sur 11.2.1 (20D74)
- CPU: Intel Core i5-10400
- RAM: Kingston HyperX Fury 16GB DDR4 + Kingston HyperX Predator RGB 16GB DDR4 @2666 Mhz
- MB: Gigabyte B460M-DS3H (Bios F3)
- GPU: XFX Radeon RX480 4GB
- SSD: Transcend MTE220S M.2 NVMe 512GB (TS512GMTE220S)
- Audio: Realtek ALC887
- WLAN & Blutooth: DW1820A CN-096JNT (BCM94350ZAE)
- OpenCore Version: 0.6.6
- SMBIOS: iMacPro1,1

What's working
- Onboard Audio ALC887
(Solution: Use layout-id = 5, Thanks to elluno91)
- USB 3.0
(Solution: Change A2AF to A3AF in USBInjectAll.kext and XHCI-unsupported.kext, Thanks to elluno91)
- Sleep / Wake
(Solution: Fix sleepimage with Hackintool)
- Wi-Fi
- Bluetooth
- AirDrop
- Handoff & Universal Clipboard
- iMessages & Other iServices
- iGPU Acceleration (Change SMBIOS to iMac20,1 and follow Comet Lake framebuffer patching: https://youtu.be/4EU8oT0-Ea8)
- Full RX480 Hardware Acceleration

What's not working / Known bugs
- DW1820A can't see 5Ghz Wi-Fi on channel 36
- Booting Windows from OpenCore picker (BSOD: ACPI_BIOS_ERROR), use Windows Boot Manager from BIOS instead
So I disabled boot picker as it is not being used.

macOS Screenshot
![catalina](https://i.ibb.co/c6xV3Wq/Screen-Shot-2563-07-02-at-12-17-02.png)
![bigsur](https://i.ibb.co/ynPBsHR/Screen-Shot-2563-11-13-at-13-49-14.png)
