# First-Time Setup & Mapping Guide


## Document Overview

This guide provides step-by-step instructions for the complete deployment and operational workflow of the V2 Pro device. It walks you through hardware setup, network configuration, map creation, and localization tasks.

## Firmware Upgrade Preparation

For optimal performance, ensure your product is running the latest firmware.  
Please firmware Upgrade procedures, please refer to:

https://github.com/Lanxin-MRDVS/V2Pro-Kit/blob/main/Document/Firmware%20Upgrade%20%26%20Device%20IP%20Modification.md

## Equipment Preparation and Setup

To complete the procedures in this guide, ensure you have the following items:

1. **V2 Pro Device:** Pre-installed on the vehicle roof.
2. **Power Supply for V2 Pro:** Direct to vehicle 24V DC or external portable supply.
3. **Computer:** A laptop with an Ethernet port and a web browser (e.g., Chrome, Edge, Firefox). No specific operating system is required. This computer is used to establish a temporary direct Ethernet connection with the V2 Pro for initial setup and mapping via the web interface. After setup, the V2 Pro operates continuously when integrated with the vehicle or fleet management system.
4. **Ethernet Cable:** for temporary connection between the V2 Pro device and the computer.

## 1. Initial Power-up and Connection

### 1.1 Power Connection and Status Verification

1. Connect the provided power supply to the V2 Pro device, following the specific wiring identification detailed in the Hardware Datasheet of Appendix A.

2. Observe the device status indicator

   - **Blue power indicator blinking slowly** → Device powered on normally
   - **No illumination** → Check wiring, and power specifications

<p align="center">
  
<img length=50% width=50% src="https://pub-7b25325ec91643989210e56dc1a181a4.r2.dev/v2pro_wp/c-1-1.png" />
<br><em>Figure 1: Power connection and status indicator</em></p>

### 1.2 Network Connection and PC Configuration

1. Physical Connection:

    Directly connect the V2 Pro to your computer via an Ethernet cable.

2. Computer Network Configuration:

    **Note:** The V2 Pro's default IP is 192.168.100.201. Ensure your computer's firewall is temporarily disabled.

    **Set a Static IP on Your Computer:**

   - IP Address: 192.168.100.XXX (XXX is any number from 2-254, except 201)
   - Subnet Mask: 255.255.255.0
   - Default Gateway: 192.168.100.1

3. Modify Device IP Address (if needed)  
    If the device IP address needs to be modified, this can be done using the GUI tool. For detailed steps, refer to Appendix E: Firmware Upgrade & Device IP Modification.

![Image placeholder: PC network configuration](https://pub-7b25325ec91643989210e56dc1a181a4.r2.dev/v2pro_wp/c-2-1.jpeg)

## 2. Web Portal Interface Overview

To access the web portal, open your web browser and enter http://192.168.100.201:9998.

**Interface Function Description:**

![Image placeholder: Web portal interface overview](https://pub-7b25325ec91643989210e56dc1a181a4.r2.dev/v2pro_wp/c-3-1.jpeg)

**Menu Bar:**

- Start Mapping: Launch mapping function
- Relocate: Perform relocalization operation
- Map Management: Map management interface
- Other function entries

**Central Panel:**

- Displays loaded 2D contour map
- Shows the real-time positioning indicator of the localization module
- Displays the real-time infrared video feed from the ceiling

**Status Panel:**

- VEHICLE real-time position coordinates (X, Y)
- Mouse coordinates on the map

## 3. Creating a Map

![Image placeholder: Creating a map](https://pub-7b25325ec91643989210e56dc1a181a4.r2.dev/v2pro_wp/c-4-1.jpeg)

### 3.1 Start Mapping

Click the **"Start Mapping"** button in the red menu bar, the system will enter mapping preparation state.

### 3.2 Enter Map Name

**Naming Rules:**

- Allowed: Letters (a-z, A-Z), numbers (0-9), underscore (_)
- **Prohibited:** Starting with numbers, special characters, spaces
- Examples: Warehouse_Aisle_01, Production_Line_B

### 3.3 Mapping Interface

When entering the mapping interface, you will see:

- Real-time laser contour display
- Mapping progress indicator

### 3.4 Mapping Best Practices

1. **Pre-planning:**

   - Plan a driving path covering the entire operational area before starting
   - Ensure the path covers all areas where the VEHICLE will actually operate
   
   **Note:** For warehouses larger than 5,000 m², we strongly recommend first driving along the perimeter of the facility, then systematically covering the internal aisles in sequence.

2. **Driving Best Practices:**

   - Low Constant Speed: Maintain steady speed of approximately 0.5 m/s
   - Straight-line Driving: Move in straight lines as much as possible
   - Right-angle Turns: Maintain 90-degree angles during turns
   - Turning in Narrow Aisles (about 2 m wide): Avoid driving to the very end of a narrow aisle before turning. Leave a distance of at least 1.5 meters from the end point and turn at a slow speed to ensure stable localization.

| Parameter | Limit | Description |
| --- | --- | --- |
| Maximum Linear Speed | ≤ 0.5 m/s | Straight motion speed limit |
| Maximum Angular Speed | ≤ 20 °/s | Rotation speed limit |
| Recommended Mapping Speed | ≈ 0.2 m/s | For optimal map quality |

3. **Coverage Strategy:**

   - Overlap Requirement: Maintain approximately **1/3 image overlap area between parallel paths**
   - Spacing Requirement: Maintain approximately **2-meter distance** between parallel paths
   - Complete Coverage: Ensure all operational areas are scanned

4. **Behaviors to Avoid:**

   - Random jitter or sudden direction changes
   - Repeated scanning of same area
   - High-speed driving or sharp turns
   - Omitting critical areas

![Image placeholder: Mapping best practices](https://pub-7b25325ec91643989210e56dc1a181a4.r2.dev/v2pro_wp/c-5-1.jpeg)

### 3.5 End Mapping

To complete the mapping process, click the "End Mapping" button in the menu bar after the VEHICLE has scanned the entire operational area. The system will then automatically process the data-processing time is proportional to the area size (large areas may take several minutes). Do not power off or operate the device during this period.

## 4. Map Management

![Image placeholder: Map management](https://pub-7b25325ec91643989210e56dc1a181a4.r2.dev/v2pro_wp/c-6-1.jpeg)

### 4.1 Local Map

1. **Apply Map:**

    In the local map interface, click **"Apply"** to activate the selected map.

2. Reboot Required:

    **Critical Step:** After clicking "Apply", you must reboot the V2 Pro device for the new map to take effect. Reboot can be performed via power cycle or software reboot.

    Failure to reboot will result in: re-localization failure, positioning errors, and unstable behavior.

3. Other Operations:

   - Export: Backup currently effective map
   - Delete: Remove map files from host

## 5. Relocalization Operation

![Image placeholder: Relocalization operation](https://pub-7b25325ec91643989210e56dc1a181a4.r2.dev/v2pro_wp/c-7-1.jpeg)

### 5.1 Start Relocalization

Click the **"Relocate"** button in the menu bar, the system enters relocalization mode.

### 5.2 Perform Relocalization

1. Automatic Map Matching:

Once started, the module automatically registers real-time LiDAR point clouds with map contours.

2. Manual Position Setting:

If automatic matching fails, drag on the map to specify an approximate position and orientation. The system uses this as the initial estimate for precise positioning.

3. Success Indicators:

   - Positioning status returns to normal
   - "Positioning timeout" error disappears
   - VEHICLE icon displays correctly on the map

### 5.3 Relocalization Tips

- Choose Feature-Rich Areas: Higher success rate in areas with distinct features like racks, corners;
- Avoid Open Areas: Relocalization is difficult in feature-sparse, open environments;
- Multiple Attempts: If unsuccessful, try relocalization at different positions;

## 6. Parameter Configuration

### 6.1 Configuration Interface Overview

Access via **"Parameter Config"** in the menu bar

## 7. Advanced Configuration & Feature Deployment

### Network Configuration

![Image placeholder: Network configuration](https://pub-7b25325ec91643989210e56dc1a181a4.r2.dev/v2pro_wp/c-8-1.jpeg)

1. **Wi-Fi Setup**  
    Access: Click “Parameter Config” → “On-Site Config” → “Wi-Fi”

    For Dynamic IP (DHCP):

   - Set wifi_name (SSID) and wifi_pwd (password).
   - Set ziwang (subnet mask) to 24.

    For Static IP:

   - address: Enter the fixed IP address.
   - gateway: Enter the network gateway.
   - static: Must be set to “yes”.

2. **Wired Ethernet Setup**

   - Default IP: 192.168.100.201
   - Computer IP must be in the same subnet (e.g., 192.168.100.10).

![Image placeholder: Wired Ethernet setup](https://pub-7b25325ec91643989210e56dc1a181a4.r2.dev/v2pro_wp/c-9-1.jpeg)

### 7.2 Communication Protocol Configuration

#### UDP Output Configuration

Access: Click “Parameter Config” → “Robot Config” → “Driver”

- portName: IP address of the system receiving pose data.
- portCode: UDP port number for communication.

### 7.3 Relocalization QR Code Deployment

**Reference link:** https://github.com/Lanxin-MRDVS/V2Pro-Kit/wiki/Relocalization-QR-Code-Deployment

**Note:** It is suggested to complete QR code deployment before mapping, ensuring tags are within the camera's FOV and meet size requirements. For the AprilTag system, tag family 36H11 is recommended.

1. **QR code and Printing Requirements**

    QR code file are provided in the archive V2Pro_QRcode_tags.zip.

    **Download link:**

    https://github.com/Lanxin-MRDVS/V2Pro-Kit/releases/download/V2-Pro-V1.2.0/V2Pro_QRcode_tags.zip

    Adhere to the following printing specifications:

   - Print the QR code on non-reflective white paper (e.g., matte adhesive paper) using a laser printer with **scaling disabled.**
   - For long-term durability, apply a matte protective film (avoid glossy finishes) over the code, to prevent reflection issues.
   - Note: The size refers to the actual QR code size, excluding any white margin.

2. **ID-to-Size Correspondence**
    
    The system automatically determines physical tag dimensions and calculates pose based on the tag ID. IDs are strictly bound to specific dimensions. Printing must conform exactly to the following requirements:

| ID Range | Physical Size (cm) |
| --- | --- |
| 000–099 | 30 |
| 100–199 | 40 |
| 200–299 | 50 |
| 300–399 | 60 |
| 400–499 | 70 |
| 500–587 | 80 |

**WARNING:** Use of non-standard tag sizes will cause localization algorithm errors and relocalization failures.
    
3. Deployment Methods  

    QR code deployment is recommended to be completed before mapping operations.

   - Method A: Horizontal on Ceiling (Recommended)

        Ensure a clear, unobstructed view - a slight tilt is acceptable.

    
   - Method B: Vertical on Walls/Columns

        Use when ceiling mounting is not feasible- a slight tilt is acceptable.

![Image placeholder: Horizontal on ceiling](https://pub-7b25325ec91643989210e56dc1a181a4.r2.dev/v2pro_wp/c-10-1.png)

![Image placeholder: Vertical on walls or columns](https://pub-7b25325ec91643989210e56dc1a181a4.r2.dev/v2pro_wp/c-11-1.png)

4. Size-to-Height Reference Table

| Relative Height(m) | QR Code size include margin (cm) | QR Code size pure black block (cm) |
| --- | --- | --- |
| < 3 | 30 | 24 |
| 4 | 40 | 32 |
| 5 | 50 | 40 |
| 6 | 60 | 48 |
| 7 | 70 | 56 |
| > 8 | 80 | 64 |

![Image placeholder: Size-to-height reference](https://pub-7b25325ec91643989210e56dc1a181a4.r2.dev/v2pro_wp/c-12-1.jpeg)

**Note:** “Relative Height” is the vertical distance between the camera and the QR code. The attached QR code files include a white margin zone (should keep it). The actual code area (dark modules) equals 80% of the file dimensions. Scale accordingly when printing.

5. Multi-Gate / Multi-Entrance Recognition

    For multi-entrance scenarios, it is recommended to deploy distinct gate/entrance QR codes.

## 8. Operational FAQs & Troubleshooting

**Q: We are testing the V2 Pro in a narrow aisle (about 2 m wide) with very few ceiling features. The vehicle is driven roughly in the center, but we notice that rotation is not smooth even at a slow angular speed. What could be the cause and how can we improve performance?**

**A:** For narrow aisles (less than 2 m wide) with sparse overhead features such as in office demonstration environments, we recommend using a special firmware version for optimal performance. Here’s why:

To reduce noise and prevent self-detection of the vehicle body, the standard V2 Pro firmware filters out LiDAR points within 1.5 m by default. In narrow aisles, especially during turns near corners, the sidewalls may fall partially or entirely inside this filtered zone. This can significantly reduce the number of usable features for localization, leading to tracking instability.

To address this, we offer a customized firmware version that reduces or disables the 1.5 m filtering range. This retains more wall data in confined spaces, thereby improving stability during rotations and cornering.

**Q: What should I do if I cannot connect to the V2 Pro via WLAN?**

**A:** This issue is typically caused by a network routing conflict, especially in environments with multiple subnets.

![Image placeholder: WLAN connection issue](https://pub-7b25325ec91643989210e56dc1a181a4.r2.dev/v2pro_wp/c-13-1.png)

Root Cause:  
The V2 Pro device operates on the 192.168.0.X subnet by default. If a client device (e.g., a PC) is on a different subnet (e.g., 192.168.2.X), the connection may fail due to incorrect routing table configuration.

Important Note:

- Devices within the same subnet (e.g., 192.168.0.X) can connect to the V2 Pro without any issues.
- The problem only occurs when crossing different subnets without proper routing.

Solution:  
Modify the Ethernet interface (eth0) IP configuration on the client side by removing the default gateway or adjusting the routing table to ensure proper communication across subnets.

Example:  
If your PC is on 192.168.2.X and you need to connect to a V2 Pro on 192.168.0.201:

- Either temporarily change your PC's IP to the same subnet (e.g., 192.168.0.X)
- Or add a static route to route traffic to 192.168.0.X via the appropriate gateway

**Q: How to reconfigure the date/time if the camera display shows an incorrect timestamp (e.g., from the previous month)?**

**A:** The HTTP API is available for time synchronization.

![Image placeholder: HTTP API time synchronization](https://pub-7b25325ec91643989210e56dc1a181a4.r2.dev/v2pro_wp/c-14-1.png)

For ROS, a clock synchronization program is currently under development and will be made available in a future release.

**Q: Under the condition that the vehicle/device was stationary during power-off, the startup time still exceeds 35 seconds. What should I check?**

**A:** Verify optimization settings:

- Check /etc/rc.local:

  - Access the device via SSH.
  - Confirm that the line containing sleep 20 has been removed. If this line is present, it will add a 20-second delay.

![Image placeholder: rc.local sleep setting](https://pub-7b25325ec91643989210e56dc1a181a4.r2.dev/v2pro_wp/c-15-1.png)

- Check /home/fr1511b/start_all.sh:

  - Confirm that all sleep commands within this script have their time arguments set to 1 (e.g., sleep 1). For example, lines like sleep 5 or sleep 10 should be changed to sleep 1.

**Note:** This issue will be fixed in the production release.

**Q: Can we use LTE during the V2 PRO testing period?**

**A:** Regarding LTE network support: Due to the complex and costly certification requirements, the V2 Pro is confirmed not to include an internal LTE module for now.

For your immediate testing and demonstration needs, we recommend the following reliable workaround:

Recommended Setup: Use a Mobile Hotspot

1. Enable the personal hotspot (Wi-Fi tethering) function on your mobile phone.
2. Connect both the V2 Pro unit and your host computer to this phone hotspot.
3. This setup provides instant internet access, enabling full functionality for testing and demos without needing to access or modify the customer's existing enterprise Wi-Fi infrastructure.

---

<p align="center">
  <sub><em>Last updated: June 2026</em></sub><br>
  <sub><em>Hangzhou Lanxin Technology Co., Ltd. & MRDVS Co., Ltd.</em></sub><br>
  <sub><em>All Rights Reserved.</em></sub>
</p>
