# V2 Pro Release Notes

[Home](../README.md) / Release Notes

This file is the consolidated English software history. Original GitHub Releases, tags, dates, and assets remain available at their existing URLs. Document revisions are tracked separately on the [homepage](../README.md#user-content-document-update-history).

<a id="v1-2-0"></a>

## V1.2.0

**GitHub publication date:** 2026-06-12 · [Original Release](https://github.com/Lanxin-MRDVS/V2Pro-Kit/releases/tag/V2-Pro-V1.2.0)

### Release Notes 20260612

#### Feature Updates

##### Interface Functions

* Removed irrelevant error messages during mapping, such as localization timeout and relocalization failure.
* Removed unrelated four-direction arrow controls during mapping.
* Added a mapping completion prompt after successful mapping.
* Ensured that newly created maps are displayed in the map list without manual refresh.
* Added a prompt after switching maps to remind users to restart the program.
* Simplified the Localization configuration items to three options.

##### Device-Side Functions

* Disabled background localization calculation during mapping to reduce resource usage.
* Improved LiDAR odometry stability during high-speed operation, especially when V2 Pro is installed facing backward.
* Fixed occasional angle drift during mapping.
* Optimized QR map generation to retain the most reliable QR coordinates.
* Fixed the QR code size adaptation issue. This version supports the previously provided 30 cm QR code template whose actual black border size is 24 cm.
* Added real-time speed calculation and display on the web interface.

#### Firmware Patch Updates

* Added`device_version.txt`to support external modification of the device version number.
* Packaged the`insmod_wifi.sh`script and added LiDAR network connectivity checking with up to three retry attempts.
* Restored the broadcast-based camera discovery function.

#### Downloads
> **Upgrade Guide:** For step-by-step firmware upgrade instructions, see [Firmware Upgrade & Device IP Modification](https://github.com/Lanxin-MRDVS/V2Pro-Kit/blob/main/Document/Firmware%20Upgrade%20%26%20Device%20IP%20Modification.md).

* Upgrade via the System WEB Portal:
  Navigate to: Software Upgrade → Firmware Update (in the left-hand menu)
  * Frontend Package: [rob0525.zip](https://github.com/Lanxin-MRDVS/V2Pro-Kit/releases/download/V2-Pro-V1.2.0/rob0525.zip)
  * Algorithm Firmware Package: [hontai_2.1.43-V2-Normal_971b8_260529A0529_200954_md5182a8.zip](https://github.com/Lanxin-MRDVS/V2Pro-Kit/releases/download/V2-Pro-V1.2.0/hontai_2.1.43-V2-Normal_971b8_260529A0529_200954_md5182a8.zip)

* Upgrade via the MRDVS GUI Software *LxCameraViewer* ([Ubuntu](https://github.com/Lanxin-MRDVS/CameraSDK/releases/download/SDK-V2.4.60/LxCameraViewer-ubuntu20-viewer.tar.gz)/[Windows](https://github.com/Lanxin-MRDVS/CameraSDK/releases/download/SDK-V2.4.60/MRDVS-2.4.60.260126-windows-installer.exe)):
  * Hardware Patch: [V2Pro-update-V1.1.2_260609.bin](https://github.com/Lanxin-MRDVS/V2Pro-Kit/releases/download/V2-Pro-V1.2.0/V2Pro-update-V1.1.2_260609.bin)
 
> **Notes:**
> 1. Due to the firmware version, the "Web Front-End" option may not appear under **Software Upgrade** in the Web portal. If this occurs, update the firmware first using the LxCameraViewer GUI with the file below. After the update, confirm that the "Web Front-End" option appears in the Web portal before proceeding with other updates.
>    * Firmware file: [V2_firmware_update_260324_V1.1.2.bin](https://github.com/Lanxin-MRDVS/V2Pro-Kit/releases/download/V2-Pro-V1.2.0/V2_firmware_update_260324_V1.1.2.bin)
> 2. As the hardware platform matures and stabilizes, subsequent firmware updates are expected to be less frequent. In most cases, future updates can be performed directly through the Web Portal.
> 3. The Frontend Package and the Algorithm Firmware Package are coupled upgrade packages for this release. To ensure version compatibility, it is recommended to upgrade both packages to the corresponding versions provided in this release.
> 4. After the upgrade, the corresponding version information can be checked on the WEB interface. The `hontai` package corresponds to the Body version, and the `rob` package corresponds to the Frontend version.

* ROS1 SDK: [V2_ROS1.zip](https://github.com/Lanxin-MRDVS/V2Pro-Kit/releases/download/V2-Pro-V1.2.0/V2_ROS1.zip)
* ROS2 SDK: [V2_ROS2.zip](https://github.com/Lanxin-MRDVS/V2Pro-Kit/releases/download/V2-Pro-V1.2.0/V2_ROS2.zip)
* Pre-defined Positioning QR Codes: [V2Pro_QRcode_tags.zip](https://github.com/Lanxin-MRDVS/V2Pro-Kit/releases/download/V2-Pro-V1.2.0/V2Pro_QRcode_tags.zip)

### Published assets

| File | Size (bytes) | Download |
| --- | ---: | --- |
| `hontai_2.1.43-V2-Normal_971b8_260529A0529_200954_md5182a8.zip` | 28,707,778 | [Download](https://github.com/Lanxin-MRDVS/V2Pro-Kit/releases/download/V2-Pro-V1.2.0/hontai_2.1.43-V2-Normal_971b8_260529A0529_200954_md5182a8.zip) |
| `rob0525.zip` | 14,641,900 | [Download](https://github.com/Lanxin-MRDVS/V2Pro-Kit/releases/download/V2-Pro-V1.2.0/rob0525.zip) |
| `V2Pro-update-V1.1.2_260609.bin` | 4,879,742 | [Download](https://github.com/Lanxin-MRDVS/V2Pro-Kit/releases/download/V2-Pro-V1.2.0/V2Pro-update-V1.1.2_260609.bin) |
| `V2Pro_QRcode_tags.zip` | 84,953 | [Download](https://github.com/Lanxin-MRDVS/V2Pro-Kit/releases/download/V2-Pro-V1.2.0/V2Pro_QRcode_tags.zip) |
| `V2_firmware_update_260324_V1.1.2.bin` | 57,142,318 | [Download](https://github.com/Lanxin-MRDVS/V2Pro-Kit/releases/download/V2-Pro-V1.2.0/V2_firmware_update_260324_V1.1.2.bin) |
| `V2_ROS1.zip` | 6,423,587 | [Download](https://github.com/Lanxin-MRDVS/V2Pro-Kit/releases/download/V2-Pro-V1.2.0/V2_ROS1.zip) |
| `V2_ROS2.zip` | 17,691,043 | [Download](https://github.com/Lanxin-MRDVS/V2Pro-Kit/releases/download/V2-Pro-V1.2.0/V2_ROS2.zip) |

<a id="v1-1-1"></a>

## V1.1.1

**GitHub publication date:** 2026-03-10 · [Original Release](https://github.com/Lanxin-MRDVS/V2Pro-Kit/releases/tag/Firmware)

The original release title contains `260318`, while its GitHub publication date is 2026-03-10. Both are retained; do not infer publication dates or component compatibility from asset filenames.

### V2 Pro Firmware
#### Version: V1.1.0 -> V1.1.1

#### Bug Fixes
- Fixed incorrect relocalization display on web interface
- Fixed relocalization error response from ROS
- Fixed occasional crash during mapping
- Fixed abnormal logging module behavior on web interface
- Fixed issue allowing multiple ROS nodes to run simultaneously
- Fixed map download incorrectly returning success for empty directories

#### Changes
- QR code localization ID now binds with print size
- Changed update method to web interface (zip upgrade package); backend packages still require host machine update (bin package)
- Updated bin package to include all web-side bin/lib files for consistency

---

**ROS1 SDK:** [Download Link](https://github.com/Lanxin-MRDVS/V2Pro-Kit/releases/download/Firmware/V2_ROS_SDK.zip)
**ROS2 SDK:** [Download Link](https://github.com/Lanxin-MRDVS/V2Pro-Kit/releases/download/Firmware/ros2_v2_1.1.2.zip)
**Pre-defined positioning QR code:** [Download Link](https://github.com/Lanxin-MRDVS/V2Pro-Kit/releases/download/Firmware/V2Pro_QRcode_tags.zip)

### Published assets

| File | Size (bytes) | Download |
| --- | ---: | --- |
| `hontai_2.1.43-V2-Normal_ad75d_260511A0511_174551_md5d2228.zip` | 28,682,176 | [Download](https://github.com/Lanxin-MRDVS/V2Pro-Kit/releases/download/Firmware/hontai_2.1.43-V2-Normal_ad75d_260511A0511_174551_md5d2228.zip) |
| `receivePTP` | 54,888 | [Download](https://github.com/Lanxin-MRDVS/V2Pro-Kit/releases/download/Firmware/receivePTP) |
| `ros2_v2_1.1.2.zip` | 17,691,043 | [Download](https://github.com/Lanxin-MRDVS/V2Pro-Kit/releases/download/Firmware/ros2_v2_1.1.2.zip) |
| `V2Pro-update-V1.1.000000_260120.bin` | 4,878,941 | [Download](https://github.com/Lanxin-MRDVS/V2Pro-Kit/releases/download/Firmware/V2Pro-update-V1.1.000000_260120.bin) |
| `V2Pro_QRcode_tags.zip` | 84,953 | [Download](https://github.com/Lanxin-MRDVS/V2Pro-Kit/releases/download/Firmware/V2Pro_QRcode_tags.zip) |
| `V2_firmware_update_260321_V1.1.1.fix.bin` | 58,482,036 | [Download](https://github.com/Lanxin-MRDVS/V2Pro-Kit/releases/download/Firmware/V2_firmware_update_260321_V1.1.1.fix.bin) |
| `V2_ROS_SDK.zip` | 6,360,539 | [Download](https://github.com/Lanxin-MRDVS/V2Pro-Kit/releases/download/Firmware/V2_ROS_SDK.zip) |

