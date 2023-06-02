# MSI-Z170-A-PRO-Hackintosh
This is an Opencore 0.9.2 version of MSI-Z170-A-PRO Hackintosh EFI. It works on macOS Ventura 13.4.

MSI-Z170-A-PRO
=============
[![](https://asset.msi.com/resize/image/global/product/five_pictures1_3571_2015090218004355e6c8cb75bf4.png62405b38c58fe0f07fcef2367d8a9ba1/1024.png)](https://www.msi.com/Motherboard/Z170-A-PRO/Specification "MSI-Z170-A-PRO")
## Working:

## Hardware
| Item | Brand | Model | Driver | Comment |
|-----|-----|-----|-----|-----|
| Motherboard | MSI | Z170-A-PRO | | |
| CPU | Intel | i5-6600K OC 4,5 Ghz | | |
| RAM | G.Skill |  Ripjaws V 2x4GB DDR4 | | |
| iGPU | Intel | HD Graphics 530 | built-in | Headless mode |
| dGPU | Sapphire | RX 570 Pulse ITX 4GB  | built-in |  |
| dGPU | XFX  | RX 460 2GB | built-in | Bios flash  to [Gigabyte.RX460](https://www.techpowerup.com/vgabios/187609/gigabyte-rx460-2048-160804)   |
| SSD | Goodram |  Cx400 128 Gb  | | |
| SSD | Adata | Premier Pro SP900  | | |
| Wireless | Fenvi | FV HB1200  Wi-Fi 2.4/5GHz and Bluetooth PCI-E Card | built-in |  |
| Ethernet | Realtek | RTL8111 | [RealtekRTL8111.kext](https://github.com/Mieze/RTL8111_driver_for_OS_X/releases) | |
| Audio | Realtek | ALC892 | [AppleALC](https://github.com/acidanthera/AppleALC) | I have broken audio card ona my motherboard |
## BIOS Setup
### Disable
- Fast Boot
- Secure Boot
- Serial/COM Port
- Parallel Port
- Compatibility Support Module (CSM).
- Thunderbolt
- Intel SGX
- CFG Lock
### Enable
- VT-x
- VT-d
- Above 4G decoding. 
- EHCI/XHCI Hand-off
- OS type: Windows 8.1/10 UEFI Mode
- Primary Display  PCIE 
- iGPU-Multi-Monitor  Enabled 
- DVMT Pre-Allocated(iGPU Memory): 64MB
- SATA Mode: AHCI
## SMBIOS FIX:
Use [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS) to generate your own unique SMBIOS. If running macOS Ventura, use a Kaby Lake SMBIOS iMac18,3.
## Note
I chose 15 USB ports in my USB map. 4x USB 3.0(back) + 2x USB 2.0(back) + Bluetooth(internal via USB 2.0) 
If booting macOS Ventura, you need to spoof your iGPU as the closest Kaby Lake model.

| Key | Type | Value |
|-----|-----|-----|
| AAPL,ig-platform-id | Data | 00001B59 |
| device-id | Data | 16590000 |

alcid=1
## Links:

[**Apple**](http://apple.com/)

[**Acidanthera**](https://github.com/acidanthera)

[**Dortania**](https://dortania.github.io/getting-started/)
