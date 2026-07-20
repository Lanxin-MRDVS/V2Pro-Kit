# MRDVS V2 Pro - Infrastructure-Free Fusion-SLAM™ Localization Module

## 1. Overview

The MRDVS V2 Pro is an all-in-one embedded localization device engineered to serve as the core positioning source for the modern digital warehouse, supporting AGVs, AMRs, and the full spectrum of Material Handling Vehicles (MHVs)—from forklifts and reach trucks to pallet trucks and tow tractors. Its compact, integrated design combines a 2D SLAM LiDAR, a ceiling-forward vision sensor, and an IMU into a single, factory-calibrated unit.

At its core is our Fusion SLAM™ technology—a tightly coupled sensor fusion algorithm and deep-learning-based engine refined through nearly ten years of real-world data collection and corner-case optimization. Built on this experience, the system continuously evaluates and weights multi-sensor data in real time, adapting to changing environmental conditions to ensure reliable, uninterrupted operation. Through the intelligent fusion of LiDAR point clouds, visual features, and IMU data, it consistently delivers stable ±3 cm localization accuracy at 10 Hz, with all processing performed onboard.

## 2. Key Applications

The V2 Pro is engineered for three core application areas: 

**1)	The Core Positioning Device for AGVs & AMRs**\
The V2 Pro provides the centimeter-accurate, infrastructure-free positioning essential for Autonomous Guided Vehicles (AGVs) and Autonomous Mobile Robots (AMRs) to execute core tasks-such as material transport, facility inspection, and industrial cleaning-with full reliability.

**2)	The Ideal Retrofit Kit for Manual-to-Autonomy Conversion**\
It serves as the complete positioning and navigation unit for transforming manual forklifts into autonomous AGVs. This enables rapid, cost-effective automation of existing assets.

**3)	The Precision Awareness Device for Manual MHVs**\
For the broader spectrum of non-autonomous material handling vehicles (MHVs) including reach trucks, pallet trucks, order pickers, tow tractors, and more, the V2 Pro provides high-precision real-time location data. This enables critical capabilities such as proximity safety alerts, accurate fleet tracking, and rich data feeds for digital twin systems, forming the intelligent sensory layer of the modern digital warehouse.

## 3. Technical Specifications

| Parameter                | Specification                                                                       |
| ------------------------ | ----------------------------------------------------------------------------------- |
| **Positioning Accuracy** | ±3 cm (up to 15m ceiling height)                                                    |
| **Update Rate**          | 10 Hz                                                                               |
| **Sensors**              | 2D LiDAR (270° FoV, 40m range), IR Camera (108°×57° FoV, 8 IR emitters), 6-axis IMU |
| **Processing**           | Onboard edge computing, no external server required                                 |
| **Map Capacity**         | Single map &gt;100,000 m²; Total storage &gt;1,000,000 m²                           |
| **Power**                | 24V DC / 3A                                                                         |
| **Interfaces**           | Gigabit Ethernet, CAN Bus (CANopen), Wi-Fi 2.4GHz, 4x Digital I/O, Audio            |
| **Environmental**        | IP54, -20°C to +60°C operating, shock-resistant for forklift mounting               |
| **Dimensions**           | 146.5 × 66.3 × 89.4 mm (excl. cables)                                               |

---
## 4. Resources

The table below lists the download entry points for V2 Pro V1.2.0. For detailed update notes, package descriptions, version compatibility information, and upgrade instructions, see the [Release Notes](https://github.com/Lanxin-MRDVS/V2Pro-Kit/releases/tag/V2-Pro-V1.2.0).

| Resource                                       | Download                                                                                                                                                 |
| ---------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Frontend Package**                           | [Download Link](https://github.com/Lanxin-MRDVS/V2Pro-Kit/releases/download/V2-Pro-V1.2.0/rob0525.zip)                                                   |
| **Algorithm Firmware Package**                 | [Download Link](https://github.com/Lanxin-MRDVS/V2Pro-Kit/releases/download/V2-Pro-V1.2.0/hontai_2.1.43-V2-Normal_971b8_260529A0529_200954_md5182a8.zip) |
| **Hardware Patch**                             | [Download Link](https://github.com/Lanxin-MRDVS/V2Pro-Kit/releases/download/V2-Pro-V1.2.0/V2Pro-update-V1.1.2_260609.bin)                                |
| **V2 Pro Integrated Firmware Upgrade Package** | [Download Link](https://github.com/Lanxin-MRDVS/V2Pro-Kit/releases/download/V2-Pro-V1.2.0/V2_firmware_update_260324_V1.1.2.bin)                          |
| **ROS1 SDK**                                   | [Download Link](https://github.com/Lanxin-MRDVS/V2Pro-Kit/releases/download/V2-Pro-V1.2.0/V2_ROS1.zip)                                                   |
| **ROS2 SDK**                                   | [Download Link](https://github.com/Lanxin-MRDVS/V2Pro-Kit/releases/download/V2-Pro-V1.2.0/V2_ROS2.zip)                                                   |
| **Pre-defined Positioning QR Codes**           | [Download Link](https://github.com/Lanxin-MRDVS/V2Pro-Kit/releases/download/V2-Pro-V1.2.0/V2Pro_QRcode_tags.zip)                                         |


## 5. System Highlights

**1) Near-Zero Infrastructure Deployment**
The system operates immediately out of the box with minimal configuration, requiring no pre-installed infrastructure such as UWB anchors, AprilTags, beacons, or reflectors. This delivers plug-and-play functionality, reducing deployment complexity, time, and cost.
Seamless Zone Transition & Rapid Relocalization
With its ceiling-forward camera, the system can instantly re-localize by scanning a QR code when transitioning between mapped areas - such as moving from outdoor yards into indoor warehouses or recovering position after movement. This ensures continuous, accurate positioning without manual intervention.

**2) Field-Proven Technology, Scaled from AMRs to Your Fleet**
Fusion-SLAM™ is field-hardened through large-scale autonomous deployments. Refined across over a hundred real-world sites, it powers critical material handling and industrial operations in diverse environments. Now, this same proven core is engineered to scale beyond dedicated AMRs.

**3) Innovative & Reliable System Architecture**
As a fully integrated embedded system designed to overcome the challenges of varied industrial environments, this device employs a tightly-coupled LiDAR-Visual-Inertial SLAM algorithm and a deep learning-enhanced vision engine. It harmonizes data from its integrated 2D LiDAR, vision sensor, and IMU within a single compact unit, delivering reliable ±3 cm accuracy whether operating in narrow aisles, dynamic storage layouts, open areas, or high-bay racking systems.

**4) Built for scale, not just precision**
The system follows a "map once, deploy everywhere" principle: only one unit is required to generate a master map, which can be distributed to all other vehicles. You don't need to map everything at once - skip areas under construction, blocked by materials, or not yet ready. Later, simply extend the existing map by adding new zones (e.g., a new workshop). The system scales flexibly as your facility evolves.

**5) Open Architecture & Intelligent Integration**
Designed for flexibility, the solution offers a browser-based web portal for intuitive setup, real-time monitoring, and remote configuration - no additional software required. 
For seamless system-level integration, the device supports industry-standard interfaces including CAN (CANopen), Gigabit Ethernet, and provides ROS/ROS 2 packages, UDP communication, MQTT communication, and HTTP APIs (supporting POST/GET methods), enabling direct and continuous feeding of precise vehicle location data into higher-level Fleet Management Systems (FMS) or Warehouse Management Systems (WMS).



## 6. Documentation

| Document                         | Link                                                                                                    |
| -------------------------------- | ------------------------------------------------------------------------------------------------------- |
| **First-Time Setup & Mapping Guide** |[View Documentation](https://github.com/Lanxin-MRDVS/V2Pro-Kit/blob/main/Document/First-Time%20Setup%20%26%20Mapping%20Guide.md)|
| **Firmware Upgrade & Device IP Modification** |[View Documentation](https://github.com/Lanxin-MRDVS/V2Pro-Kit/blob/main/Document/Firmware%20Upgrade%20%26%20Device%20IP%20Modification.md)|
| **HTTP Communication Protocol**  | [View Documentation](https://github.com/Lanxin-MRDVS/V2Pro-Kit/wiki/V2-Pro-HTTP-Communication-Protocol) |
|**MQTT Communication Protocol**   |[View Documentation](https://github.com/Lanxin-MRDVS/V2Pro-Kit/wiki/V2-Pro-MQTT-communication-protocal )|
| **UDP Communication Protocol**   | [View Documentation](https://github.com/Lanxin-MRDVS/V2Pro-Kit/wiki/V2-Pro-UDP-Communication-Protocol)  |
| **ROS1 Interface Documentation** | [View Documentation](https://github.com/Lanxin-MRDVS/V2Pro-Kit/wiki/V2-Pro-ROS1-Interface)              |
| **ROS2 Interface Documentation** | [View Documentation](https://github.com/Lanxin-MRDVS/V2Pro-Kit/wiki/V2-Pro-ROS2-Interface)              |
| **Relocalization QR Code Deployment** |[View Documentation](https://github.com/Lanxin-MRDVS/V2Pro-Kit/wiki/Relocalization-QR-Code-Deployment)|


