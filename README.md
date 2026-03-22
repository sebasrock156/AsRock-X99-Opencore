[OpenCore Legacy Patcher]: https://github.com/dortania/OpenCore-Legacy-Patcher/releases

# AsRock X99 Extreme4/11 or Extreme6/Taichi Opencore (Tahoe 26.X)

![Tahoe](https://i.imgur.com/kA4LqPA.png)

### Works:
---
<details>

- Installer Boot ✅ (Installation on SATA: ~30/35 minutes | Installation on Nvme: ~20/25)

- System Boot ✅

- USB Ports ✅❌ (USB 3.0 ports are recognized but, try to remap with UTB).

- Screen ✅ (1336x768, 1080x1920)

- Ethernet ✅ (Intel ports only)

- Audio ✅❌ (You need reinstall AppleHDA.kext with @perez987 's [repository](https://github.com/perez987/AppleHDA-back-on-macOS-26-Tahoe) and @Mirone 's [MyKextInstaller](https://github.com/Mirone/MyKextInstaller)

- PCI Express Ports (M.2 Port included, Nvmefix kext it's added; RAM modules are recognized as "PCI devices")✅

- Sleep Mode ✅❌ (Only works suspend mode, but in "wakelock" state).

- Front COM Port (It's detected) ✅
 
</details>


### IMPORTANT NOTES:
---

## For fix HDA Audio (in-built):

1. Disable AMFI from config.plist (my [release]() EFI is done).
2. Follow the guide by @Mirone from [here](https://github.com/Mirone/MyKextInstaller).
3. If audio doesn't work patch your EFI build with SSDT-HPET and add the boot-args: *-lilubetaall* and *-alcbeta*.

## For use AMD Graphics only:

1. Add the boot-arg:

- "**radpg=15**" for enabling 3D Acceleration (In almost all 2016 or older GPUs, Eg: R9 Fury X, HD 7730, etc).

- "**agdpmod=pikera**" for try enabling drivers (In almost all 2018 or newer GPUs, Eg: Vega 56, RX 5700XT, RX 6600, etc).
From *NVRAM --> 7C436110-AB2A-4BBB-A880-FE41995C9F82*

***This isn't necessary with Polaris (10/20/30) and Vega 21 (Eg. Radeon VII) graphic cards.***

2. Rename the "**model** key" by yours in **PciRoot(0x0)/Pci(0x1,0x0)/Pci(0x0,0x0)** and **PciRoot(0x0)/Pci(0x1,0x0)/Pci(0x0,0x1)**" from *DeviceProperties* with your graphic card data (Eg: AMD Radeon RX 5700XT and Bermuda HDMI Audio [Navi Series])

---

## For use Nvidia Graphics only:

1. Add the boot-arg "**nv_disable=1**" (for using Vesa drivers); later, create a new table like this (for enabling Nvidia Drivers):

![nvidiatable](https://i.imgur.com/1crQGj1.png)

**Usually for Pascal (GTX1000 Series), Maxwell (GTX900 Series) and Kepler (GTX600/700 Series) GPUs.***

all on *NVRAM --> 7C436110-AB2A-4BBB-A880-FE41995C9F82*; if Nvidia GPU isn't recognize after that, add "**agdpmod=pikera**" boot-arg too.

2. Rename the "**model** key" by yours in **PciRoot(0x0)/Pci(0x1,0x0)/Pci(0x0,0x0)** and **PciRoot(0x0)/Pci(0x1,0x0)/Pci(0x0,0x1)**" from *DeviceProperties* (Eg: Nvidia GeForce GTX 1070Ti and Nvidia HDMI Output)

3. Download and install [OpenCore Legacy Patcher] for try patch your GPU (Pascal *GTX1000* and older generations *GTX900, 700, 600* are supported; **ALL RTX MODELS AREN'T SUPPORTED**), later, go to *config.plist --> NVRAM --> 7C436110-AB2A-4BBB-A880-FE41995C9F82* and remove "**nv_disable=1**" and reboot.

---




