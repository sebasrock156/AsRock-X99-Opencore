[OpenCore Legacy Patcher]: https://github.com/dortania/OpenCore-Legacy-Patcher/releases

# AsRock X99 Extreme4/11 or Extreme6/Taichi Opencore (Sonoma 14.X)

![Screenshot](https://i.imgur.com/ffR1lDH.png)

### Works:
---
<details>

- Installer Boot ✅ (Installation on SATA: ~30/35 minutes | Installation on Nvme: ~20/25)

- System Boot ✅

- USB Ports (All ports are 2.0)✅

- Screen ✅ (1336x768, 1080x1920)

- Audio Card ✅ (Inputs and Outputs)

- Ethernet ✅

- PCI Express Ports (M.2 Port included, Nvmefix kext it's added)✅

- Sleep Mode ✅

- Front COM Port (It's detected) ✅
 
</details>


### IMPORTANT NOTES:
---

## For use AMD Graphics only:

1. Add the boot-arg:

- "**radpg=15**" for enabling 3D Acceleration (In almost all 2017 or older GPUs, Eg: RX 580, RX 470, R9 Fury X, HD 7730, etc).

- "**agdpmod=pikera**" for try enabling drivers (In almost all 2018 or newer GPUs, Eg: Vega 56, Radeon VII, RX 5700XT, RX 6600, etc).
From *NVRAM --> 7C436110-AB2A-4BBB-A880-FE41995C9F82*

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




