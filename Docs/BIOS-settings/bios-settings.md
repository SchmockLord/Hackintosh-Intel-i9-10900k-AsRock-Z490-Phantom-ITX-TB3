# My BIOS-settings

Some BIOS-settings are recommended for the Z490 platform in general, and some BIOS-settings depend on wether you use the iMac20,2 or the iMacPro1,1 config.

## Disable 
(reference: https://dortania.github.io/OpenCore-Install-Guide/config.plist/comet-lake.html#disable):
- Fast Boot
- Secure Boot
- VT-d (can be enabled if you set DisableIoMapper to YES)
- CSM
- Intel SGX
- Intel Platform Trust
- CFG Lock (MSR 0xE2 write protection)(This must be off, if you can't find the option then enable both AppleCpuPmCfgLock and AppleXcpmCfgLock under Kernel -> Quirks. Your hack will not boot with CFG-Lock enabled)

## Enable 
(reference: https://dortania.github.io/OpenCore-Install-Guide/config.plist/comet-lake.html#enable):
- VT-x
- Above 4G decoding
- Hyper-Threading
- Execute Disable Bit
- EHCI/XHCI Hand-off
- OS type: Windows 8.1/10 UEFI Mode
- DVMT Pre-Allocated(iGPU Memory): 64MB
- SATA Mode: AHCI


## iMac20,2-specific settings:
- Primary Graphics Adapter: PCIE (when you plugin the monitor in the graphics card) or iGPU (when you plugin the monitor to your onboard HDMI)
- Share Memory: 64MB
- IGPU Multi-Monitor: Enabled (this keeps the iGPU enabled even when a graphics card is detected)

## iMacPro1,1-specific settings:
- Primary Graphics Adapter: PCIE (with iMacPro1,1 config, the iGPU is disabled)
- Share Memory: 64MB
- IGPU Multi-Monitor: Disabled (iGPU is disabeld when a graphics card is detected)

Here are screenshot of the most relevant BIOS-settings. Screenshots were taken with BIOS version 1.40A (currently Beta BIOS).

I am not saying that you have to set every setting exactly like I did. Just so you know what works for me :).

![My BIOS-setting 1](/Docs/BIOS-settings/IMG_1111.jpg)

![My BIOS-setting 2](/Docs/BIOS-settings/IMG_1129.jpg)

![My BIOS-setting 3](/Docs/BIOS-settings/IMG_1130.jpg)

![My BIOS-setting 4](/Docs/BIOS-settings/IMG_1112.jpg)

![My BIOS-setting 5](/Docs/BIOS-settings/IMG_1113.jpg)

![My BIOS-setting 6](/Docs/BIOS-settings/IMG_1114.jpg)

![My BIOS-setting 7](/Docs/BIOS-settings/IMG_1115.jpg)

![My BIOS-setting 8](/Docs/BIOS-settings/IMG_1116.jpg)

![My BIOS-setting 9](/Docs/BIOS-settings/IMG_1117.jpg)

![My BIOS-setting 10](/Docs/BIOS-settings/IMG_1118.jpg)

![My BIOS-setting 11](/Docs/BIOS-settings/IMG_1119.jpg)

![My BIOS-setting 12](/Docs/BIOS-settings/IMG_1120.jpg)

![My BIOS-setting 13](/Docs/BIOS-settings/IMG_1121.jpg)

![My BIOS-setting 14](/Docs/BIOS-settings/IMG_1122.jpg)

![My BIOS-setting 15](/Docs/BIOS-settings/IMG_1123.jpg)

![My BIOS-setting 16](/Docs/BIOS-settings/IMG_1124.jpg)

![My BIOS-setting 17](/Docs/BIOS-settings/IMG_1125.jpg)

![My BIOS-setting 18](/Docs/BIOS-settings/IMG_1126.jpg)

![My BIOS-setting 19](/Docs/BIOS-settings/IMG_1127.jpg)

![My BIOS-setting 20](/Docs/BIOS-settings/IMG_1128.jpg)
