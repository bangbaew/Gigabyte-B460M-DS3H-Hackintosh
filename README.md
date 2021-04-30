My Build
- OS: macOS Big Sur 11.3 (20E232)
- CPU: Intel Core i5-10400 / i7-10700
- RAM: Kingston HyperX Fury 16GB DDR4 + Kingston HyperX Predator RGB 16GB DDR4 @2666 Mhz
- MB: Gigabyte B460M-DS3H (Bios F5d)
- GPU: XFX Radeon RX480 4GB
- SSD: Transcend MTE220S M.2 NVMe 512GB (TS512GMTE220S)
- Audio: Realtek ALC887
- WLAN & Blutooth: DW1820A CN-096JNT (BCM94350ZAE)
- OpenCore Version: 0.6.8
- SMBIOS: iMac20,1

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
- iGPU Acceleration (Solution: Use SMBIOS iMac20,1)
- Full RX480 Hardware Acceleration
- Dual Boot Windows from OpenCore (Disable DSDT.aml)

What's not working / Known bugs
- DW1820A can't see 5Ghz Wi-Fi on channel 36
- Using HDMI on iGPU (Intel UHD 630) gives black screen.

macOS Screenshot
![catalina](https://i.ibb.co/c6xV3Wq/Screen-Shot-2563-07-02-at-12-17-02.png)
![bigsur](https://i.ibb.co/ynPBsHR/Screen-Shot-2563-11-13-at-13-49-14.png)
