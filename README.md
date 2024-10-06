# ✨ Asus-Vivobook-X515EA-Hackintosh (Intel i3 1115G4) 🌌
## 🌿 System Specification
| Name | Description |
| - | - |
| CPU | Intel 11th Gen Tiger Lake Core i3-1115G4 3.00 GHz |
| Chipsets | Intel Tiger Lake-LP |
| Graphics | Intel UHD Graphics |
| Memory | LPDDR4x 3200 MHz 20GB |
| Sound | Realtek HD Audio ALC 256 |
| Wi-Fi / Bluetooth | Intel Wi-Fi 6 AX201 160MHz |

## 🍃 Installed macOS & OpenCore Versions
- macOS Catalina 10.15.7
- macOS Big Sur 11.x
- macOS Monterey 12.x
- macOS Ventura 13.x
- macOS Sonoma 14.x
- OpenCore r1.0.1

## 🍁 BIOS Settings
- Boot
  - Secure Boot Control : `Off`
  - Fast BIOS Mode : `Off`
- Using RU.efi
  - CpuSetup `(VarStore : 0x2)`
    - CFG Lock `(Variable : 0x43)` : Disabled `(Value : 0x0)`
  - SaSetup `(VarStore : 0x5)`
    - DVMT Pre-Allocated Memory `(Variable : 0x84)` : 64MB `(Value : 0x2)`
    - CD Clock Frequency `(Variable : 0x47)` : 648 MHz `(Value : 0x7)` / 652.8 MHz `(Value : 0x8)`
      - Even though I used RU.efi to force CD Clock Frequency to 648 MHz or higher in BIOS settings, `-igfxcdc` boot arg is still required.

## ⚠️ Attention
- Intel Iris Xe Graphics iGPU is not supported by macOS and QE/CI acceleration is not available. [Discussion #15](https://github.com/lshbluesky/Samsung-NT750XDA-KF59U-Hackintosh/discussions/15)
  - Therefore, it is difficult to actually use macOS on Intel 11th Gen Tiger Lake systems.

## ✅ Working
- [X] Realtek ALC 256 ComboJack Headphone
- [X] Realtek ALC 256 ComboJack Microphone
- [X] Speed Step (XCPM, Partially working)
- [X] Intel Wi-Fi 6 AX201 160MHz
- [X] Intel AX201 Bluetooth
- [X] USB 3.x & USB Port Map
- [X] Integrated Webcam
- [X] Samsung I2C Precision TouchPad (Polling Mode Only)
- [X] Intel Iris Xe Graphics G7 QE/CI

## ❌ Not Working
- [ ] Realtek ALC 256 Internal Speaker
- [ ] Realtek ALC 256 Internal Microphone
- [ ] Complete/Full Power Management
- [ ] Brightness Control
- [ ] Fn Keys (Brightness & Sound Volume Control)
- [ ] Battery Percentage Indication
- [ ] Sleep & Wake
