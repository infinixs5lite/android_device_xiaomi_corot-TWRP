# [WIP] TWRP device tree for REDMI K60 ULTRA

[WIP] 注意：本项目编译出的 vendor_boot 还在测试阶段，无法正常启动！
=========================================
## Thanks @YuKongA

REDMI K60 ULTRA (codenamed _"corot"_) 

## Device specifications

Basic   | Spec Sheet
-------:|:-------------------------
SoC     | MediaTek Dimensity 9200+ (MT6985Z)
CPU     | 1x 3.35 GHz Cortex-X3, 3x 3.0 GHz Cortex-A715, 4x 2.0 GHz Cortex-A510
GPU     | Immortalis-G715 MC11, 1164 MHz, 
Memory  | 12/16/24 GB RAM , 4266 MHZ
Shipped Android Version | 13.0 with MIUI 14
Storage | 256/512/1024 GB
Battery | 5000 mAh, Li-Polymer
Camera  | 9280 x 6920 pixels, 7680 x 4320 pixels, 24 fps
SIM Card | Nano-SIM, Nano-SIM / microSD
Positioning | GPS, A-GPS, BeiDou, Glonass, Galileo, NavIC    

## Features

Works:

 -: preparatory phase for the project
## Getting Started ##
To get started with AOSP sources to build TWRP, you'll need to get familiar
with [Git and Repo](https://source.android.com/source/using-repo.html).

To initialize your local repository using the AOSP trees to build TWRP, use a command like this:

    repo init -u https://github.com/corot-scrapyard/android_device_xiaomi_corot-TWRP.git -b twrp-12.1
To initialize a shallow clone, which will save even more space, use a command like this:

    repo init --depth=1 -u https://github.com/corot-scrapyard/android_device_xiaomi_corot-TWRP.git -b twrp-12.1
Then to setup the build:
    
    cd <source-dir>; export ALLOW_MISSING_DEPENDENCIES=true; . build/envsetup.sh; lunch twrp_<device>-eng

Build command that applies:

- Vendor_boot image ramdisk: `mka vendorbootimage`

## To use it:

```
fastboot flash vendor_boot vendor_boot.img
```
## Device picture
![corot](https://i02.appmifile.com/329_operator_sg/14/08/2023/3fcfdc0e83081349795e70056be19e35.png)
