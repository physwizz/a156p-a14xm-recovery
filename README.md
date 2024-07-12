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

Here's a revised and improved version of your README snippet:

**### Build**

Make sure you have the necessary build environment set up, including Android build tools and the LineageOS source code.

1. **Preparation:**
   ```bash
   chmod +x mkbootimg  # Ensure mkbootimg script is executable
   source build/envsetup.sh  # Source the build environment setup script
   export ALLOW_MISSING_DEPENDENCIES=true  # Optional, allows building with missing dependencies
   lunch twrp_a14xm-eng  # Choose the appropriate device/variant for your A14XM phone (replace 'a14xm' if different)
   ```

2. **Build Recovery Image:**
   ```bash
   mka recoveryimage
   ```

**Troubleshooting:**

If you encounter the following error during the build process:

```
[100% 2/2] ----- Making recovery image ------
FAILED: out/target/product/a14xm/recovery.img
...
```

This usually indicates an issue with permissions or the execution of the `mkbootimg` script. Ensure the following:

* **Permissions:** You've made `mkbootimg` executable using `chmod +x mkbootimg`.
* **Environment:** You've sourced the build environment setup script (`build/envsetup.sh`).
* **Device:** You've selected the correct device/variant using `lunch`.
* **Dependencies:**  All required build dependencies are installed.



