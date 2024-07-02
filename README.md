# Xeon 2680v3 - Kllisre X99-FD4 (C620) - SOYO RX 580 2048SP - ALC887

## Opencore 1.0.0
![Image](https://i.imgur.com/OrT3nY8.png)

## :computer: Hardware:

| **Category** | **Component**                                                                    |
| ------------ | -------------------------------------------------------------------------------- |
| **CPU**      | 2,5 GHZ Intel Xeon 2680v3 (12/24) (Haswell-E)                                  |
| **GPU**      | SOYO - AMD Radeon RX 580 2048SP 8GB                                            |
| **RAM**      | 16GB DDR4 2133MHZ Kllisre                                                      |
| **CHIPSET**  | C620 (Kllisre X99-FD4)                                                         |
| **SSD**      | 240GB Kingston SATA (Dual Boot W11/macOS 14)                                   |
| **Wi-Fi** | TP-Link TL-WN823N                                                                 |
| **Ethernet** | Realtek RTL8111                                                                |
| **Audio**    | Realtek ALC897 (layout-id=11)                                                    |


## :white_check_mark: Working:

- [x] CPU power management
- [x] Graphics acceleration
- [x] Keyboard & Mouse
- [x] Wi-Fi
- [x] USB ports
- [x] HDMI video & audio output
- [x] Ethernet
- [x] Audio (Internal speakers, 3.5mm headphone jack)
- [x] AirDrop & Handoff
- [x] iCloud & App Store
- [x] iMessage & FaceTime

## 🛠️ Kexts:

- [x] AppleALC
- [x] AppleMCEReporterDisabler
- [x] CpuTscSync
- [x] Lilu
- [x] RealtekRTL8111
- [x] RestrictEvents
- [x] RtWlanU
- [x] RtWlanU1827
- [x] SMCProcessor
- [x] SMCSuperIO
- [x] USBMap
- [x] VirtualSMC
- [x] WhateverGreen

## :x: Not working:
     
- [x] Native Wi-Fi & Bluetooth
- [x] Sleep

## :closed_lock_with_key: SMBIOS

MacPro7,1 or iMacPro1,1 (using MacPro7,1 in this EFI)

Use GenSMBIOS to generate your own unique SMBIOS and then copy each parameter following the path (recommended to follow the guide above): [Fixing iServices](https://dortania.github.io/OpenCore-Post-Install/universal/iservices.html)

Config.plist -> PlatformInfo -> Generic

## Intel BIOS settings

### Disable
- Fast Boot
- Secure Boot
- Serial/COM Port
- Parallel Port
- VT-d (can be enabled if you set DisableIoMapper to YES)
- Compatibility Support Module (CSM) (Must be off in most cases, GPU errors/stalls like gIO are common when this option is enabled)
- Thunderbolt
- Intel SGX
- Intel Platform Trust
- CFG Lock (MSR 0xE2 write protection)

### Enable
- VT-x
- Above 4G Decoding
- If experiencing issues, ensure "MMIOH Base" is set to 12 TB or lower
- Hyper-Threading
- Execute Disable Bit
- EHCI/XHCI Hand-off
- OS type: Windows 8.1/10 UEFI Mode (some motherboards may require "Other OS" instead)
- SATA Mode: AHCI

## Credits

- [OpenCore Install Guide](https://dortania.github.io/OpenCore-Install-Guide/)
- [chris1111 Wireless USB Adapter](https://github.com/chris1111/Wireless-USB-OC-Big-Sur-Adapter)
- [Apple](https://apple.com)
