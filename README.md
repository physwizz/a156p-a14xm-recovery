# Android Device Tree for Samsung SM-A146P (a14xm)

```
#
# Copyright (C) 2024 The LineageOS Project
#
# SPDX-License-Identifier: Apache-2.0
#
```

![banner](https://i.blogs.es/37c09e/product-image_galaxy-a14-5g/1366_521.jpg)

## Overview

The Samsung Galaxy A14 5G is an entry level device released by Samsung in early 2023 featuring MediaTek's Dimensity 700 chipset

## Specifications

### Hardware

- **Processor**: MediaTek Dimensity 700 (7 nm)
- **RAM**: 4GB LPDDRX4 
- **Storage**: Internal storage options range from 64GB to 128GB, expandable storage. (UFS 2.2)
- **Display**: 6.6-inch PLS LCD with a resolution of 1080 x 2408 pixels and a 90Hz refresh rate.
- **Battery**: 5000mAh
- **Camera**:
  - Triple rear camera setup: 50MP wide, 2MP macro, and 2MP depth sensor.
  - 32MP front-facing camera.
- **Connectivity**:
  - Network: GSM / HSPA / LTE / 5G
  - Wi-Fi: Wi-Fi 802.11 a/b/g/n/ac, dual-band, Wi-Fi Direct
  - Bluetooth: 5.2, A2DP, LE
  - NFC: Yes
  - USB: USB Type-C 2.0
- **Sensors**: Fingerprint (side-mounted), accelerometer, gyro, proximity, compass

### Build 
- run chmod +x mkbootimg, otherwise you will run into the following problems:
[100% 2/2] ----- Making recovery image ------
FAILED: out/target/product/a14xm/recovery.img
/bin/bash -c "(device/samsung/a14xm/mkbootimg --ramdisk out/target/product/a14xm
/ramdisk-recovery.img  --cmdline \"androidboot.init_fatal_reboot_target=recovery
 buildvariant=eng\" --base 0x40078000 --pagesize 2048 --recovery_dtbo device/sam
sung/a14xm/prebuilt/dtbo.img --dtb out/target/product/a14xm/dtb.img 
--kernel out
/target/product/a14xm/kernel 
--os_version 12 --os_patch_level 2099-12-31 --kerne
l_offset 0x00008000 --pagesize 2048 --ramdisk_offset 0x11088000 --second_offset 
0x07c00000 --tags_offset 0x07c08000 --dtb  --output out/target/product/a14xm/rec
overy.img ) && (echo \"----- Lying about SEAndroid state to Samsung bootloader -
-----\" ) && (echo -n \"SEANDROIDENFORCE\" >> out/target/product/a14xm/recovery.
img ) && (echo \"Made recovery image: out/target/product/a14xm/recovery.img\" ) 
&& (tar -C out/target/product/a14xm -c recovery.img > out/target/product/a14xm/r
ecovery.tar ) && (echo \"Made flashable out/target/product/a14xm/recovery.tar: o
ut/target/product/a14xm/recovery.img\" )"

'bash
source build/envsetup.sh; export ALLOW_MISSING_DEPENDENCIES=true; lunch twrp_a12-eng;  '

'mka recoveryimage '

