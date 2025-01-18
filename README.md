[AirportItlwm]: https://github.com/openintelwireless/itlwm/releases
[Itlwm]: https://openintelwireless.github.io/itlwm/Installation.html
[USBToolBox]: https://github.com/USBToolBox/tool
[guide1]: https://elitemacx86.com/threads/how-to-enable-thunderbolt-3-hotplug-on-macos.462/
[guide2]: https://elitemacx86.com/threads/how-to-enable-thunderbolt-on-macos.461/

# AsRock X99 Extreme4/11 or Extreme6/Taichi Opencore (Monterey - Sequoia?)

> ⚠ **ADVICE** ⚠: For USB Type-C try to fix with [USBToolBox] and for fix Thunderbolt follow these: [guide1] and [guide2].
---

## Motherboards comparison

Hardware | Extreme4 | Extreme11 | Extreme6 | Taichi 
--- | --- | --- | --- | :--: 
Motherboard | [![MoBoE4](https://i.imgur.com/Q8CgiQa.png)](https://www.asrock.com/mb/intel/x99%20extreme4/) | [![MoBoE11](https://i.imgur.com/VLlZ4QH.png)](https://www.asrock.com/MB/Intel/X99%20Extreme11/index.asp) | [![MoBoE6](https://i.imgur.com/XReX76F.png)](https://www.asrock.com/MB/Intel/X99%20Extreme6/index.asp) | [![MoBoTai](https://i.imgur.com/VszqKuM.png)](https://www.asrock.com/MB/Intel/X99%20Taichi/index.asp)
![bios](https://i.imgur.com/RmYixFt.png) | Aptio's V v3.80 (by American Megatrends (AMI/AsRock) | Aptio's V v3.40 (by American Megatrends (AMI/AsRock) | Aptio's V v3.50 (by American Megatrends (AMI/AsRock) | Aptio's V v1.80 (by American Megatrends (AMI/AsRock)
![processor](https://i.imgur.com/K9VlfRK.png) | Intel Xeon (5th Gen) E5-2640v4 10 Cores/20 Threads@2,4Ghz | Intel Xeon (5th Gen) E5-2630v4 10 Cores/20 Threads@2,2Ghz | Intel Xeon (5th Gen) E5-2650v4 12 Cores/24 Threads@2,2Ghz | Intel Xeon (5th Gen) E5-2690v4 14 Cores/28 Threads@2,6Ghz
![dgpu](https://i.imgur.com/7TZmF2e.png) | AMD/Sapphire Radeon RX 580 Nitro+ 8GB VRAM | Gigabyte RX 570 GamingX 4GB VRAM | XFX Radeon RX 5700XT 8GB VRAM | Sapphire Radeon RX 5600 Pulse 6GB VRAM
![audio](https://i.imgur.com/A7RRuUn.png) | ALC1150 Purity Sound 2 | ALC1150 Purity Sound 2 | ALC1150 Purity Sound 2 | ALC1150 Purity Sound 3
Ethernet | Intel I218V | Intel I218V (main) and Intel I211AT (2nd) | Intel I218V (main) and Qualcomm Atheros AR8171 (2nd, not supported since OSX Mojave)| Intel I218V (main) and Intel I211AT (2nd)
![wlan](https://i.imgur.com/9eDLwo9.png) | N/A | N/A | Add a Intel Wireless card | Add [AirportItlwm] for Monterey or Ventura / [Itlwm] for BigSur, Sonoma or Sequoia?)
![ddr4](https://i.imgur.com/2oda3vY.png) | Corsair ValueSelect 32GB(4x8GB) DDR4@2133Mhz | Corsair ValueSelect 32GB(4x8GB) DDR4@2133Mhz | Corsair ValueSelect 32GB(4x8GB) DDR4@2133Mhz | Corsair ValueSelect 64GB(8x8GB) DDR4@2400Mhz
![ssd](https://i.imgur.com/pozDx4X.png) | Kingston A400 240GB (TLC PS3111 Controller, testing drive) | Idem | Idem | Idem 
![nvme](https://i.imgur.com/xbsV0Ia.png) | Kioxia Exceria Pro 1TB SSD Nvme (TLC PS5018 Controller) | Idem | Idem | Idem
USB Ports | 4 USB 2.0 (rear)/2 USB 2.0 connectors (frontal), 4 USB 3.1 (rear)/1 USB 3.1 connector (frontal); OSX is limited to 11 USB Inputs | 4 USB 2.0 (rear)/2 USB 2.0 connectors (frontal), 4 USB 3.1 (rear)/2 USB 3.1 connectors (frontal); OSX is limited to 11 USB Inputs | 2 USB 2.0 (rear)/2 USB 2.0 connectors (frontal)/1 USB 2.0 connector (internal), 6 USB 3.1 (rear)/2 USB 3.1 connectors (frontal); OSX is limited to 11 USB Inputs | 3 USB 2.0 (rear)/2 USB 2.0 connectors (frontal), 4 USB 3.1 (rear)/1 USB 3.1 connector (frontal), 1 USB Type-C 3.1 (rear); OSX is limited to 11 USB Inputs
---


I'm bringing another OpenCore EFI, now for these X99 motherboards, for more information, click on "More info of **MacOS Version** below:


**More info of MacOS Monterey:**

[![MacOS Monterey](https://i.imgur.com/xcZ2v8a.png)](https://github.com/sebasrock156/AsRock-X99-Opencore/tree/Monterey)

**Status:** Done ✅ (test with [Release EFI](https://github.com/sebasrock156/AsRock-X99-Opencore/releases) )🖥

**More info of MacOS Ventura:**

[![MacOS Ventura](https://i.imgur.com/KvpKPLD.png)](https://github.com/sebasrock156/AsRock-X99-Opencore/tree/Ventura)

**Status:** Done ✅ (test with [Release EFI](https://github.com/sebasrock156/AsRock-X99-Opencore/releases) )🖥

**More info of MacOS Sonoma:**

[![MacOS Sonoma](https://i.imgur.com/q5X0WXd.png)](https://github.com/sebasrock156/AsRock-X99-Opencore/tree/Sonoma)

**Status:** Done ✅ (test with [Release EFI](https://github.com/sebasrock156/AsRock-X99-Opencore/releases) )🖥

**More info of MacOS Sequoia (doesn't exist even):**

[![MacOS Sequoia](https://i.imgur.com/EzZuom8.png)](https://github.com/sebasrock156/AsRock-X99-Opencore/tree/Sequoia)

**Status:** In plaining 👷‍♂️




