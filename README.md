# macOS Sonoma - MSI Prestige 15 A10SC-056FR - EFI

This repository contains a fully functional EFI folder for installing **macOS Sonoma** on the **MSI Prestige 15 A10SC-056FR**.

**Powered by OpenCore 1.0.6** - Future-proof bootloader with upgrade capabilities.

## ⚠️ macOS Sequoia Compatibility Notice

> **Note about macOS Sequoia**: This EFI has been tested on macOS Sequoia, but encountered significant issues:
> - ❌ **Bluetooth**: Not working at all
> - ⚠️ **WiFi**: Only worked sporadically through [HeliPort](https://github.com/OpenIntelWireless/HeliPort), with unreliable connectivity
> 
> **For this reason, I recommend staying on macOS Sonoma**, which offers proven stability and full wireless functionality. Sometimes a slightly older macOS version with complete hardware support is preferable to the latest release with compromised features.

## 💻 Hardware Specifications

| Component | Details |
|-----------|---------|
| **Model** | MSI Prestige 15 A10SC-056FR |
| **Processor** | Intel Core i7-10710U (6 cores, 12 threads, 1.1 GHz / 4.7 GHz Turbo, 12 MB cache) |
| **Integrated Graphics** | Intel UHD Graphics 630 |
| **Discrete Graphics** | NVIDIA GeForce GTX 1650 Max-Q (4 GB GDDR5) |
| **Memory** | 16 GB DDR4-2666 MHz (1 x 16 GB, upgradable to 32 GB) |
| **Storage** | 512 GB SSD PCIe NVMe M.2 (2 slots available) |
| **Display** | 15.6" Full HD (1920 x 1080) IPS, matte finish, 60 Hz |
| **WiFi & Bluetooth** | Wi-Fi 6 (802.11ax), Bluetooth 5.0 | (Intel AX 201)
| **Audio** | 2 speakers (2x2W) |
| **Ports** | 2x USB 3.2 Type-C (1 with Thunderbolt), 2x USB 3.2, HDMI, Audio combo jack |


## 🚀 OpenCore Version

- **OpenCore**: 1.0.6
- **Recommended macOS**: Sonoma (fully tested and stable)
- **Tested but not recommended**: Sequoia (wireless issues)

This EFI is built with OpenCore 1.0.6, ensuring compatibility with current and future macOS releases. OpenCore's modular architecture makes it easy to update and maintain your Hackintosh over time.

## ✨ Features

- ✅ **Fully functional EFI** - Ready to use for macOS Sonoma installation
- ✅ **WiFi working** - Native Wi-Fi 6 support (on Sonoma)
- ✅ **Bluetooth working** - Bluetooth 5.0 fully functional (on Sonoma)
- ✅ **Graphics acceleration** - Intel UHD Graphics properly configured
- ✅ **Audio** - Full audio support
- ✅ **Battery management** - Working power management
- ✅ **USB ports** - All USB ports functional
- ✅ **Trackpad** - Multitouch gestures supported
- ✅ **Future-proof** - OpenCore 1.0.6 allows easy updates to newer macOS versions

## ⚙️ Configuration Required

Before using this EFI, you **must** generate your own unique device properties:

1. Download [ProperTree](https://github.com/corpnewt/ProperTree)
2. Download [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS)
3. Follow the [Dortania OpenCore Install Guide](https://dortania.github.io/OpenCore-Install-Guide/) to generate proper SMBIOS information
4. Update the `config.plist` file with your generated values

> **Important**: Do NOT use this EFI without generating your own device properties first!

## 🔧 BIOS Settings

Before installing macOS, make sure to configure your BIOS settings properly:

### Disable:
- **Secure Boot** → Must be disabled
- **Fast Boot** → Must be disabled
- **CSM/Legacy Boot** → Should be disabled

### Enable:
- **UEFI Boot Mode**
- **AHCI Mode** for SATA

> ⚠️ **Warning**: Incorrect BIOS settings will prevent your Hackintosh from booting properly!

## 📥 Installation

1. Create a macOS Sonoma bootable USB drive following the [Dortania guide](https://dortania.github.io/OpenCore-Install-Guide/)
2. Clone or download this repository
3. Generate your SMBIOS data using GenSMBIOS
4. Update the `config.plist` with your generated values using ProperTree
5. Copy the EFI folder to your USB drive's EFI partition
6. Configure BIOS settings as listed above
7. Boot from the USB drive and install macOS Sonoma

# Boot Issues Troubleshooting

If you experience boot difficulties (more than 3 minutes with a black screen), please update your boot arguments with the following: alcid=3 -wegnoegpu igfxonln=1 igfxfw=2 darkwake=0
This should resolve the issue and allow your system to boot normally.

## 🔄 Updating OpenCore

Thanks to OpenCore 1.0.6, this EFI can be easily updated to support future macOS versions:

1. Download the latest OpenCore release
2. Update the bootloader files in the EFI folder
3. Review and merge any new configuration options
4. Test thoroughly before upgrading macOS

Refer to the [OpenCore Upgrade Guide](https://dortania.github.io/OpenCore-Post-Install/universal/update.html) for detailed instructions.

## 📚 Resources

- [Dortania OpenCore Install Guide](https://dortania.github.io/OpenCore-Install-Guide/)
- [OpenCore Documentation](https://github.com/acidanthera/OpenCorePkg)
- [ProperTree](https://github.com/corpnewt/ProperTree)
- [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS)

## ⚠️ Disclaimer

- This EFI configuration is provided as-is
- Creating a Hackintosh is for educational purposes only
- macOS is designed to run on Apple hardware
- Always backup your data before installation
- I am not responsible for any damage to your hardware

## 📝 License

This project is for educational purposes only.

---

**Note**: If you find this EFI helpful, please star ⭐ this repository!

If this repository helped you and you'd like to show your appreciation, feel free to buy me a coffee! ☕

**Bitcoin**: bc1qefqhr4fflza3g4hccsskams4yrk6v2z06pr4ya
