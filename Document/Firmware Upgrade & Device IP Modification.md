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

Download the latest Firmware update package at:

https://github.com/Lanxin-MRDVS/V2Pro-Kit/releases

1. Firmware package name: hontai_update_xxxxxx_Vxxx.bin \
(currently we are using [V2Pro-update-V1.1.2_260609.bin](https://github.com/Lanxin-MRDVS/V2Pro-Kit/releases/download/V2-Pro-V1.2.0/V2Pro-update-V1.1.2_260609.bin))

<img alt="Näyttökuva 2026-06-22 kello 17 04 02" src="https://github.com/user-attachments/assets/c1b53371-2362-494b-a24a-220bbb843256" />


Modify Device IP Address (if needed)

If the target device requires a different IP address, it can also be modified using the GUI tool (see screenshot below).

<img alt="PixPin_2026-06-22_11-31-33" src="https://github.com/user-attachments/assets/c1b5d20e-d982-4ab3-8769-d7941124d292" />


IP Configuration

Make sure the computer's network IP address is configured as instructed in 1.2 Network Connection and PC Configuration.

### 1.2 Run the GUI Tool and update the firmware

**Reference link:** https://github.com/Lanxin-MRDVS/V2Pro-Kit/wiki/Mapping-User-Guide-Step-by-Step#4-firmware-update

Launch the installed ***LxCameraViewer.exe*** software, then follow the instructions shown in the images to upgrade the firmware;

<img alt="PixPin_2026-06-22_11-55-14" src="https://github.com/user-attachments/assets/d4f8bd72-77b1-4ad3-ba15-bb1320125fcc" />


![e-4-2.jpeg](https://pub-7b25325ec91643989210e56dc1a181a4.r2.dev/v2pro_wp/e-4-2.jpeg)

The upgrade process takes approximately one minute. Once complete, reopen the device in the **Device List** and check **Device Information** to verify the firmware version has been successfully updated.

## 2. Mapping Algorithm Firmware Update (via Web Portal)

The online update feature for mapping algorithm firmware is now supported via the Web Portal. 

### 2.1 Preparetion

Download the latest Front-end update package and Algorithm update firmware at:

https://github.com/Lanxin-MRDVS/V2Pro-Kit/releases

1. Front-end update package: [rob0525.zip](https://github.com/Lanxin-MRDVS/V2Pro-Kit/releases/download/V2-Pro-V1.2.0/rob0525.zip)
2. Algorithm update firmware: [hontai_2.1.43-V2-Normal_971b8_260529A0529_200954_md5182a8.zip](https://github.com/Lanxin-MRDVS/V2Pro-Kit/releases/download/V2-Pro-V1.2.0/hontai_2.1.43-V2-Normal_971b8_260529A0529_200954_md5182a8.zip

<img alt="Näyttökuva 2026-06-22 kello 18 12 44" src="https://github.com/user-attachments/assets/dc2f0ce2-e0f4-4780-9a82-307686c232ea" />

### 2.2 Run the Web Platform and update the front-end and algorithm

Connect the V2 Pro camera system with your PC, then launch the system management platform via Web Portal at http://192.168.100.201:9998 .

#### Step 1: Click [Web-Frontend] tab and then click [Single Vehicle Web Frontend Package Upload] button
<img alt="PixPin_2026-06-22_12-33-13" src="https://github.com/user-attachments/assets/2adb8103-0674-4f77-8f84-7370ecc3b7b6" />

#### Step 2: Click [Select Single Vehicle Web Frontend Package] button and select the frontend update package mentioned above

<img alt="PixPin_2026-06-22_12-33-45" src="https://github.com/user-attachments/assets/a1a6a3d7-4f4e-44c3-86b5-a2df0e8a72f5" />

#### Step 3: Select the right package and then click [Upload] button

<img alt="PixPin_2026-06-22_12-34-41" src="https://github.com/user-attachments/assets/54ca0316-c900-4c4a-b5b7-ed497497d361" />
<img alt="PixPin_2026-06-22_12-35-11" src="https://github.com/user-attachments/assets/1b5ee3e7-f455-4a9c-b894-a0e9b300d015" />

After uploading the front-end update package, the front-end will be updated automatically.

#### Step 4: Click [Firmware Update] button and then click [View Package (local)] button
<img width="1901" height="926" alt="PixPin_2026-06-22_12-37-09" src="https://github.com/user-attachments/assets/83676cb4-e494-4fae-9b7f-27d78b07dda7" />

#### Step 5: Click [Select File] button
<img alt="PixPin_2026-06-22_12-37-34" src="https://github.com/user-attachments/assets/1089ce67-2e61-462c-8ae2-8572d5516b16" />

#### Step 6: Select the right algorithm firmware update package and then click [Upload] button 
<img  alt="PixPin_2026-06-22_12-38-02" src="https://github.com/user-attachments/assets/538f933b-f03a-4b6a-a33d-f04fe0c595d9" />

<img  alt="PixPin_2026-06-22_12-38-35" src="https://github.com/user-attachments/assets/2e25685f-9d7e-475f-83dd-f9efce8c8f94" />



After uploading the algorithm firmware update package, the Algorithm firmware will be updated automatically. 

---

<p align="center">
  <sub><em>Last updated: June 2026</em></sub><br>
  <sub><em>Hangzhou Lanxin Technology Co., Ltd. & MRDVS Co., Ltd.</em></sub><br>
  <sub><em>All Rights Reserved.</em></sub>
</p>
