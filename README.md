# Hackintosh OpenCore + Intel Alder Lake Core i7-12700F + Gigabyte B660M Aorus Pro DDR4 + Radeon RX 6800

---

| Bootloader | Version | Boot Mode | SMBIOS    | macOS   | Version    | Release Date |
|:----------:|:-------:|:---------:|:---------:|:-------:|:----------:|:------------:|
| OpenCore   | 0.9.3   | UEFI      | MacPro7,1 | Ventura | 13.4.1 (c) | 29/06/2023   |

---

<img src="https://github.com/phenkk/Hackintosh-i7-12700F-B660M-RX-6800/blob/1ea53a038c859236d32bbb7b066575ff566e093c/Docs/1-1.png" width="350">

<img src="https://github.com/phenkk/Hackintosh-Intel-Alder-Lake-B660M-AMD-Radeon-RX-6800/blob/c2183136ad31350f56b3266795ec624b471bb995/Docs/2-updt.png" width="500">
<img src="https://github.com/phenkk/Hackintosh-Intel-Alder-Lake-B660M-AMD-Radeon-RX-6800/blob/8bca6d9920ddcf3952a0131b630fe039663d6a62/Docs/3-update.png" width="500">
<img src="https://github.com/phenkk/Hackintosh-Intel-Alder-Lake-B660M-AMD-Radeon-RX-6800/blob/8bca6d9920ddcf3952a0131b630fe039663d6a62/Docs/4-update.png" width="500">

<img src="https://github.com/phenkk/Hackintosh-Intel-Alder-Lake-Gigabyte-B660M-Aorus-Pro-DDR4-Navi-23/blob/08cb7c47418a5e157ec16122f405048dd01074f9/Docs/5.jpg" width="250"> <img src="https://github.com/phenkk/Hackintosh-Intel-Alder-Lake-B660M-AMD-Radeon-RX-6800/blob/87cbb3ad1b3b653d274ececf035db88c70ab73ef/Docs/6.jpg" width="250">

Geekbench result [[link]](https://browser.geekbench.com/v5/cpu/17970607)

## Specifications:

- 12th Gen Intel Alder Lake Core i7-12700F [[link]](https://www.intel.com/content/www/us/en/products/sku/134592/intel-core-i712700f-processor-25m-cache-up-to-4-90-ghz/specifications.html)

- Gigabyte B660M Aorus Pro DDR4 [[link]](https://www.gigabyte.com/Motherboard/B660M-AORUS-PRO-DDR4-rev-10#kf)
  
  - Audio Realtek [ALC897](https://github.com/acidanthera/AppleALC/wiki/Supported-codecs) `alcid=11`
  
  - Intel Ethernet 2.5GbE LAN l225-V

- G.Skill Trident Z Neo DDR4 F4-3600C16D-32GTZN [[link]](https://www.gskill.com/product/165/326/1562839473/F4-3600C16D-32GTZN)

- Gigabyte AORUS Radeon RX 6800 MASTER 16G [[link]](https://www.gigabyte.com/Graphics-Card/GV-R68AORUS-M-16GD#kf)

- Samsung 980 Pro NVMe (Windows 11) [[link]](https://www.samsung.com/us/computing/memory-storage/solid-state-drives/980-pro-pcie-4-0-nvme-ssd-500gb-mz-v8p500b-am/)

- WD Black SN850 NVMe (macOS 13 Ventura) [[link]](https://www.westerndigital.com/products/internal-drives/wd-black-sn850-nvme-ssd#WDS500G1X0E)

- Crucial MX500 SATA SSD 1TB (Storage) [[link]](https://www.crucial.com/products/ssd/crucial-mx500-ssd)

- Midasforce SATA SSD 1TB (Storage) [[link]](https://midasforce.com/product/midasforce-ssd-super-lightning)

- Broadcom BCM9430 PCIe Adapter WIFI + Bluetooth [[link]](https://www.tokopedia.com/galericomputerba/bcm943602cs-pci-e-wifi-bluetooth-4-0-dekstop-hackintosh?extParam=ivf%3Dfalse%26src%3Dsearch)

- Xiaomi Mi 2K Gaming Monitor 27 165Hz [[link]](https://www.mi.com/global/product/mi-2k-gaming-monitor-27/)

- Lenovo Gaming Monitor G27-20 Full HD 144Hz [[link]](https://www.lenovo.com/id/in/monitors/G27-20/)

- Asus ROG Eye S [[link]](https://rog.asus.com/streaming-kits/rog-eye-s-model/)

- dbE 1080p Webcam [[link]](https://www.tokopedia.com/dbeofficial/dbe-c100-full-hd-1080p-webcam-30-fps-glass-lens-2mp-autofocus)

- Enermax Revolution D.F. 650W 80+ Gold Full-Modular [[link]](https://www.enermax.com/en/products/revolution-d.f.-650w)

- Deepcool Macube 110 White Case [[link]](https://www.deepcool.com/products/Cases/fulltowercases/Macube-110-White-Micro-ATX-Case/2021/4669.shtml)

- All Fan and AIO by Thermalright

---

## What's Working:

- [x] iServices (iCloud, iMessage, FaceTime, AirDrop, AirPlay, Handoff, Apple Watch to Unlock, ~~SideCar~~)

- [x] Hardware Acceleration

- [x] Ethernet

- [x] WIFI

- [x] Bluetooth

- [x] Audio In/Out (Motherboard and Front Panel)

- [x] All USB Ports

- [x] Power Management

- [x] Hardware Acceleration

- [x] DRM

- [x] Sleep/Wake/Restart/Shut Down

- [x] DisplayPort Audio (HDMI Audio not tested yet)

- [x] Boot-chime

- [x] Stage Manager (Ventura)

- [x] Continuity Camera (Ventura)

- [x] etc.

---

## What isn't Working:

- Nothing

---

## Guide:

1. Read, learn, and understand the Dortania's [OpenCore Install Guide](https://dortania.github.io/OpenCore-Install-Guide/) and this [Reddit](https://www.reddit.com/r/hackintosh/comments/sp1zgv/opencore_alder_lake_12thgen_intel_hackintosh/?utm_source=share&utm_medium=web2x&context=3) post.
   
   - Setup follow [Comet Lake Configs](https://dortania.github.io/OpenCore-Install-Guide/config.plist/comet-lake.html)
   - SMBIOS used `MacPro7,1`

2. ACPI Table:
   
   | SSDT              | Method                                                                                                                        | Description             |
   | ----------------- |:-----------------------------------------------------------------------------------------------------------------------------:| ----------------------- |
   | SSDT-AWAC.aml     | [Prebuilt](https://github.com/dortania/Getting-Started-With-ACPI/blob/master/extra-files/compiled/SSDT-AWAC.aml)              | Required                |
   | SSDT-EC-USBX.aml  | [Manual](https://dortania.github.io/Getting-Started-With-ACPI/Universal/ec-methods/manual.html#edits-to-the-sample-ssdt)      | Required                |
   | SSDT-GPRW.aml     | [Prebuilt](https://github.com/dortania/OpenCore-Post-Install/blob/master/extra-files/SSDT-GPRW.aml)                           | Required for Sleep/Wake |
   | SSDT-HPET.aml     | [SSDTTime](https://dortania.github.io/Getting-Started-With-ACPI/Universal/irq.html)                                           | Optional                |
   | SSDT-PLUG-ALT.aml | [Prebuilt](https://github.com/acidanthera/OpenCorePkg/blob/master/Docs/AcpiSamples/Source/SSDT-PLUG-ALT.dsl)                  | Required                |
   | SSDT-SBUS.aml     | [Manual](https://dortania.github.io/Getting-Started-With-ACPI/Universal/smbus-methods/manual.html#edits-to-the-sample-ssdt)   | Optional                |
   | SSDT-NVME-DISABLE | [Manual](https://dortania.github.io/Getting-Started-With-ACPI/Desktops/desktop-disable.html#finding-the-acpi-path-of-the-gpu) | Optional                |
   | SSDT-RHUB.aml     | [Manual](https://dortania.github.io/Getting-Started-With-ACPI/Universal/rhub-methods/manual.html)                             | Optional                |
   
   **Note:** *I recommend to manually dumping your DSDT and compile your own SSDT using [SSDTTIme](https://github.com/corpnewt/SSDTTime) (Windows/Linux).*

3. EFI Folder Structure:
   
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
         │   ├── SSDT-NVME-DISABLE.aml
         │   ├── SSDT-PLUG-ALT.aml
         │   ├── SSDT-RHUB.aml
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
         │   ├── AppleIntelI210Ethernet.kext
         │   ├── CPUFriend.kext
         │   ├── CPUFriendDataProvider.kext
         │   ├── CpuTopologyRebuild.kext
         │   ├── Lilu.kext
         │   ├── NVMeFix.kext
         │   ├── RadeonSensor.kext
         │   ├── RestrictEvents.kext
         │   ├── SMCProcessor.kext
         │   ├── SMCRadeonGPU.kext
         │   ├── SMCSuperIO.kext
         │   ├── USBToolBox.kext
         │   ├── UTBMap.kext
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
   
   `boot-args` > `-v agdpmod=pikera e1000=0 keepsyms=1 debug=0x100 -ctrsmt`

---

## Fixing & Tweaking:

- Fix Sleep/Wake:
  
  - [SSDT-GPRW.aml](https://github.com/dortania/OpenCore-Post-Install/blob/master/extra-files/SSDT-GPRW.aml)
  
  - `ACPI` > `Patch` [change Method (GPRW,2,N) to XPRW, pair with SSDT-GPRW.aml](https://github.com/dortania/OpenCore-Post-Install/blob/master/extra-files/GPRW-Patch.plist)
  
  - `ACPI` > `Patch` Change `ADBG to XDBG`:
    
    | TableSignature | OemTableId   | TableLength | Find             | Replace          | Count | Enabled | Comment             |
    |:--------------:|:------------:|:-----------:|:----------------:|:----------------:|:-----:|:-------:|:-------------------:|
    | 53534454       | 475357417070 | 0           | 4303141941444247 | 4303141958444247 | 1     | true    | Change ADBG to XDBG |

- Fix Intel Alder Lake CPU Frequency by using CPUFriendDataProvider.kext provided [here](https://github.com/dortania/bugtracker/issues/190)

- Disable SMBIOS injection into "non-Apple" OSes (ex. Windows) if you boot through OpenCore boot picker, but it breaks Bootcamp compatibility.
  
  - `Kernel` > `Quirks` > `CustomSMBIOSGuid` > `True` (default `False`)
  
  - `PlatformInfo` > `UpdateSMBIOSMode` > `Custom` (default `Create`)

- Disable Windows or other operating system from OpenCore Boot Menu.
  
  - `Misc` > `Security` > `ScanPolicy` > `2687747` (default `0`)

- Disable Radeon Zero RPM (Optional):
  
  - Just follow this [Github guide](https://github.com/perez987/RX6600XT-on-macOS-Monterey-and-PowerPlayTable)

- I noticed high disk usage, beachballing cursor after system idle because macOS keep trying to read NTFS (Windows) drive where it's my Samsung 980 Pro NVMe. So I decide to disable that drive by compiling `SSDT-NVME-DISABLE.aml` or you can try to unmounted the Windows drive every boot to macOS.

---

### BIOS:

**Note:** *Load Optimized Default Settings first before making any BIOS settings. In my case I just need to change the option like shown below, as other needed options has enabled/disabled by default.*

| Motherboard                    | Gigabyte B660M Aorus Pro DDR4 Rev. 1.0 |
|:------------------------------ | -------------------------------------- |
| BIOS Version                   | F6<br/>Checksum: 8CF0                  |
| BIOS Date                      | 12/08/2022                             |
| Extreme Memory Profile (X.M.P) | Profile 1                              |
| Windows 10 Features            | Other OS                               |

* Disabled:
  
  + Intel Platform Trust Technology (PTT) (Optional)
  
  + Secure Boot
  
  + Serial Port
  
  + APP Center Download & Install
  
  + LEDs in System Power On State (Optional)

* Enabled:
  
  - Hyper-Threading
  + Above 4G Decoding
  
  + Re-Size BAR Support

---

## Credits:

- [OpenCore Dortania](https://dortania.github.io/OpenCore-Install-Guide/)

- [OpenCore Alder Lake (12th-Gen Intel) Hackintosh Guidance](https://www.reddit.com/r/hackintosh/comments/sp1zgv/opencore_alder_lake_12thgen_intel_hackintosh/?utm_source=share&utm_medium=web2x&context=3https://www.reddit.com/r/hackintosh/comments/sp1zgv/opencore_alder_lake_12thgen_intel_hackintosh/?utm_source=share&utm_medium=web2x&context=3)

- [XFX RX 6600 XT on macOS Monterey and Zero RPM with SoftPowerPlayTable](https://github.com/perez987/RX6600XT-on-macOS-Monterey-and-PowerPlayTable)
