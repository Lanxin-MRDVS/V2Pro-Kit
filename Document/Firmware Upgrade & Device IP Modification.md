# Firmware Upgrade & Device IP Modification

The system firmware consists of two components, each with a different update method:

**Embedded Firmware** - includes low-level drivers and system firmware. This can be updated using the **GUI tool** (available for Windows and Ubuntu).

Note: Future upgrades will be rare.

**Mapping Algorithm Firmware** - includes SLAM and localization algorithms. Online updates via the Web Portal are supported, provided the firmware version is V1.1.1 or later.

## 1. Embedded Firmware Update (via GUI Tool)

### 1.1 Preparation

**Reference link:** https://github.com/Lanxin-MRDVS/V2Pro-Kit/wiki/Mapping-User-Guide-Step-by-Step#1-install-the-software-and-prepare-the-sdk-files

Download the GUI Tool

https://github.com/Lanxin-MRDVS/CameraSDK/releases

![e-1-1.png](https://pub-7b25325ec91643989210e56dc1a181a4.r2.dev/v2pro_wp/e-1-1.png)

Note:

The Windows version is recommended as it offers greater stability.

The GUI tool is only required for firmware updates - it is not needed for normal system operation.

Download the latest Firmware

https://github.com/Lanxin-MRDVS/V2Pro-Kit/releases

Firmware Name: hontai_update_xxxxxx_Vxxx.bin

![e-2-1.png](https://pub-7b25325ec91643989210e56dc1a181a4.r2.dev/v2pro_wp/e-2-1.png)

Modify Device IP Address (if needed)

If the target device requires a different IP address, it can also be modified using the GUI tool (see screenshot below).

![e-3-1.png](https://pub-7b25325ec91643989210e56dc1a181a4.r2.dev/v2pro_wp/e-3-1.png)

IP Configuration

Make sure the computer's network IP address configurated as instructed in 1.2 Network Connection and PC Configuration.

### 1.2 Run the GUI Tool and update the firmware

**Reference link:** https://github.com/Lanxin-MRDVS/V2Pro-Kit/wiki/Mapping-User-Guide-Step-by-Step#4-firmware-update

Launch the installed ***LxCameraViewer.exe*** software, then follow the instructions shown in the images to upgrade the firmware;

![e-4-1.jpeg](https://pub-7b25325ec91643989210e56dc1a181a4.r2.dev/v2pro_wp/e-4-1.jpeg)

![e-4-2.jpeg](https://pub-7b25325ec91643989210e56dc1a181a4.r2.dev/v2pro_wp/e-4-2.jpeg)

The upgrade process takes approximately one minute. Once complete, reopen the device in the **Device List** and check **Device Information** to verify the firmware version has been successfully updated.

## 2. Mapping Algorithm Firmware Update (via Web Portal)

The online update feature for mapping algorithm firmware is now supported via the Web Portal. Specific update instructions will be added later.

For any questions regarding algorithm updates, please contact our technical support team.

---

<p align="center">
  <sub><em>Last updated: June 2026</em></sub><br>
  <sub><em>Hangzhou Lanxin Technology Co., Ltd. & MRDVS Co., Ltd.</em></sub><br>
  <sub><em>All Rights Reserved.</em></sub>
</p>
