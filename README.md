# Hackintosh OpenCore + Intel Alder Lake Core i7-12700F + Gigabyte B660M Aorus Pro DDR4 + Radeon RX 6600 XT

---

| Bootloader | Version | SMBios    | macOS    | Version | Release Date |
|:----------:|:-------:|:---------:|:--------:|:-------:|:------------:|
| OpenCore   | 0.8.3   | MacPro7,1 | Monterey | 12.5.1  | 25/08/2022   |

---
![alt text](https://github.com/phenkk/Hackintosh-Intel-Alder-Lake-Gigabyte-B660M-Aorus-Pro-DDR4-Navi-23/blob/08cb7c47418a5e157ec16122f405048dd01074f9/Docs/1.png =250x)
![alt text](https://github.com/phenkk/Hackintosh-Intel-Alder-Lake-Gigabyte-B660M-Aorus-Pro-DDR4-Navi-23/blob/08cb7c47418a5e157ec16122f405048dd01074f9/Docs/2.png)
![alt text](https://github.com/phenkk/Hackintosh-Intel-Alder-Lake-Gigabyte-B660M-Aorus-Pro-DDR4-Navi-23/blob/08cb7c47418a5e157ec16122f405048dd01074f9/Docs/3.png)
![alt text](https://github.com/phenkk/Hackintosh-Intel-Alder-Lake-Gigabyte-B660M-Aorus-Pro-DDR4-Navi-23/blob/08cb7c47418a5e157ec16122f405048dd01074f9/Docs/4.png)
![alt text](https://github.com/phenkk/Hackintosh-Intel-Alder-Lake-Gigabyte-B660M-Aorus-Pro-DDR4-Navi-23/blob/08cb7c47418a5e157ec16122f405048dd01074f9/Docs/5.jpg)
![alt text](https://github.com/phenkk/Hackintosh-Intel-Alder-Lake-Gigabyte-B660M-Aorus-Pro-DDR4-Navi-23/blob/08cb7c47418a5e157ec16122f405048dd01074f9/Docs/6.jpg)

## Specifications:

- 12th Gen Intel Alder Lake Core i7-12700F [[link]](https://www.intel.com/content/www/us/en/products/sku/134592/intel-core-i712700f-processor-25m-cache-up-to-4-90-ghz/specifications.html)

- Gigabyte B660M Aorus Pro DDR4 [[link]](https://www.gigabyte.com/Motherboard/B660M-AORUS-PRO-DDR4-rev-10#kf)
  
  - Audio Realtek ALC897
  
  - Intel Ethernet 2.5GbE LAN l225-V

- Kingston Fury Beast 16GB Dual Channel DDR4 3200MHz [[link]](https://www.kingston.com/en/memory/gaming/kingston-fury-beast-ddr4-memory)

- XFX Speedster Qick AMD Radeon RX 6600 XT 8GB [[link]](https://www.xfxforce.com/shop/xfx-speedster-qick-308-amd-radeon-tm-rx-6600-xt-black)

- Samsung 980 Pro NVMe 500GB (Windows 11) [[link]](https://www.samsung.com/us/computing/memory-storage/solid-state-drives/980-pro-pcie-4-0-nvme-ssd-500gb-mz-v8p500b-am/)

- WD Black SN850 NVMe 500 GB (macOS 12) [[link]](https://www.westerndigital.com/products/internal-drives/wd-black-sn850-nvme-ssd#WDS500G1X0E)

- Midasforce SSD SATA 1TB (Storage) [[link]](https://midasforce.com/product/midasforce-ssd-super-lightning)

- Broadcom BCM9430 PCIe Adapter WIFI + Bluetooth [[link]](https://www.tokopedia.com/galericomputerba/bcm943602cs-pci-e-wifi-bluetooth-4-0-dekstop-hackintosh?extParam=ivf%3Dfalse%26src%3Dsearch)

- Lenovo Gaming Monitor G27-20 Full HD 144Hz [[link]](https://www.lenovo.com/id/in/monitors/G27-20/)

- dbE 1080p Webcam [[link]](https://www.tokopedia.com/dbeofficial/dbe-c100-full-hd-1080p-webcam-30-fps-glass-lens-2mp-autofocus)

- Enermax Revolution D.F. 650W 80+ Gold Full-Modular [[link]](https://www.enermax.com/en/products/revolution-d.f.-650w)

- Deepcool Macube 110 White Case [[link]](https://www.deepcool.com/products/Cases/fulltowercases/Macube-110-White-Micro-ATX-Case/2021/4669.shtml)

---

## What's Working:

- [x] iServices (iCloud, iMessage, FaceTime, AirDrop, AirPlay, Handoff, Apple Watch to Unlock, ~~SideCar~~)

- [x] Hardware Acceleration

- [x] Ethernet

- [x] WIFI

- [x] Bluetooth

- [x] Audio In/Out

- [x] All USB Ports

- [x] Power Management

- [x] Hardware Acceleration

- [x] DRM

- [x] Sleep/Wake/Restart/Shut Down

- [x] DisplayPort Audio (HDMI Audio not tested yet)

- [x] Boot-chime

- [x] etc.

---

## What isn't Working:

- Nothing

---

## Guide:

1. Read, learn, and understand the Dortania's [OpenCore Install Guide](https://dortania.github.io/OpenCore-Install-Guide/) and this [Reddit](https://www.reddit.com/r/hackintosh/comments/sp1zgv/opencore_alder_lake_12thgen_intel_hackintosh/?utm_source=share&utm_medium=web2x&context=3) post.
   
   - Setup follow [Comet Lake Configs](https://dortania.github.io/OpenCore-Install-Guide/config.plist/comet-lake.html)
   - SMBios used `MacPro7,1`

2. My ACPI Table:
   
   | SSDT              | Method                                                                                                                            | Description             |
   | ----------------- |:---------------------------------------------------------------------------------------------------------------------------------:| ----------------------- |
   | SSDT-AWAC.aml     | [Manual](https://dortania.github.io/Getting-Started-With-ACPI/Universal/awac-methods/manual.html#determining-which-ssdt-you-need) | Required                |
   | SSDT-EC-USBX.aml  | [Manual](https://dortania.github.io/Getting-Started-With-ACPI/Universal/ec-methods/manual.html#edits-to-the-sample-ssdt)          | Required                |
   | SSDT-GPRW.aml     | [Prebuilt](https://github.com/dortania/OpenCore-Post-Install/blob/master/extra-files/SSDT-GPRW.aml)                               | Required for Sleep/Wake |
   | SSDT-HPET.aml     | [SSDTTime](https://dortania.github.io/Getting-Started-With-ACPI/Universal/irq.html)                                               | Optional                |
   | SSDT-PLUG-ALT.aml | [Prebuilt](https://github.com/acidanthera/OpenCorePkg/blob/master/Docs/AcpiSamples/Source/SSDT-PLUG-ALT.dsl)                      | Required                |
   | SSDT-SBUS.aml     | [Manual](https://dortania.github.io/Getting-Started-With-ACPI/Universal/smbus-methods/manual.html#edits-to-the-sample-ssdt)       | Optional                |
   
   **Note:** I recommend to manually dumping your DSDT and compile your own SSDT. You can use [SSDTTIme](https://github.com/corpnewt/SSDTTime) (Windows) or [MaciASL](https://github.com/acidanthera/MaciASL) (macOS).

3. My EFI Folder Structure:
   
   ```
   ─ EFI
     ├── BOOT
     │   └── BOOTx64.efi
     └── OC
         ├── ACPI
         │   ├── SSDT-AWAC.aml
         │   ├── SSDT-EC-USBX.aml
         │   ├── SSDT-GPRW.aml
         │   ├── SSDT-HPET.aml
         │   ├── SSDT-PLUG-ALT.aml
         │   └── SSDT-SBUS.aml
         ├── Drivers
         │   ├── AudioDxe.efi
         │   ├── OpenCanopy.efi
         │   ├── OpenHfsPlus.efi
         │   ├── OpenRuntime.efi
         │   ├── ResetNvramEntry.efi
         │   └── ToggleSipEntry.efi
         ├── Kexts
         │   ├── AirportBrcmFixup.kext
         │   ├── AppleALC.kext
         │   ├── CPUFriend.kext
         │   ├── CPUFriendDataProvider.kext
         │   ├── CpuTopologyRebuild.kext
         │   ├── Lilu.kext
         │   ├── NVMeFix.kext
         │   ├── RestrictEvents.kext
         │   ├── SMCProcessor.kext
         │   ├── SMCSuperIO.kext
         │   ├── USBMap.kext
         │   ├── VirtualSMC.kext
         │   └── WhateverGreen.kext
         ├── Resources
         |   ├── Audio
         |   ├── Font
         |   ├── Image
         |   │   └── Acidanthera
         |   │       ├── Chardonnay
         |   │       ├── GoldenGate
         |   │       └── Syrah
         |   └── Label
         ├── Tools
         |   └── OpenShell.efi
         ├── config.plist
         └── OpenCore.efi
   ```

4. `NVRAM` > `7C436110-AB2A-4BBB-A880-FE41995C9F82`
   
   `boot-args` > `agdpmod=pikera e1000=0 keepsyms=1 debug=0x100 -v`

---

## Fixing & Tweaking:

- Fix Sleep/Wake:
  
  - [SSDT-GPRW.aml](https://github.com/dortania/OpenCore-Post-Install/blob/master/extra-files/SSDT-GPRW.aml)
  
  - `ACPI` > `Patch` [change Method (GPRW,2,N) to XPRW, pair with SSDT-GPRW.aml](https://github.com/dortania/OpenCore-Post-Install/blob/master/extra-files/GPRW-Patch.plist)
  
  - `ACPI` > `Patch` Change `ADBG to XDBG`:
    
    | TableSignature | OemTableId   | TableLength | Find             | Replace          | Count | Enabled | Comment             |
    |:--------------:|:------------:|:-----------:|:----------------:|:----------------:|:-----:|:-------:|:-------------------:|
    | 53534454       | 475357417070 | 0           | 4303141941444247 | 4303141958444247 | 1     | true    | Change ADBG to XDBG |

- Fix High CPU Usage after Wake:
  
  - `Kernel` > `Quirks` > `AppleXcpmCfgLock` [Disabled]

- Disable Radeon Zero RPM (Optional):
  
  - Just follow this [Github guide](https://github.com/perez987/RX6600XT-on-macOS-Monterey-and-PowerPlayTable)

---

### BIOS:

**Note:** *Load Optimized Default Settings first before making any BIOS settings. In my case I just need to change the option like shown below, as other needed options has enabled/disabled by default.*

| Motherboard                    | Gigabyte B660M Aorus Pro DDR4 Rev. 1.0 |
| ------------------------------ | -------------------------------------- |
| BIOS Version                   | F6<br/>Checksum: 8CF0                  |
| BIOS Date                      | 12/08/2022                             |
| Extreme Memory Profile (X.M.P) | Profile 1                              |
| Windows 10 Features            | Other OS                               |

* Disabled:
  
  + Intel Platform Trust Technology (PTT)
  
  + Secure Boot
  
  + Serial Port
  
  + APP Center Download & Install
  
  + LEDs in System Power On State (Optional) ~~just for aesthetic of my PC lol~~

* Enabled:
  
  - Hyper-Threading
  + Above 4G Decoding
  
  + Re-Size BAR Support

---

## Credits:

- [OpenCore Dortania](https://dortania.github.io/OpenCore-Install-Guide/)

- [OpenCore Alder Lake (12th-Gen Intel) Hackintosh Guidance](https://www.reddit.com/r/hackintosh/comments/sp1zgv/opencore_alder_lake_12thgen_intel_hackintosh/?utm_source=share&utm_medium=web2x&context=3https://www.reddit.com/r/hackintosh/comments/sp1zgv/opencore_alder_lake_12thgen_intel_hackintosh/?utm_source=share&utm_medium=web2x&context=3)

- [XFX RX 6600 XT on macOS Monterey and Zero RPM with SoftPowerPlayTable](https://github.com/perez987/RX6600XT-on-macOS-Monterey-and-PowerPlayTable)
