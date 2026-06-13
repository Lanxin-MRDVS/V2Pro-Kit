# MRDVS V2 Pro - Infrastructure-Free Fusion-SLAM™ Localization Module

## Overview

The MRDVS V2 Pro is the all-in-one embedded localization device engineered as the core positioning source for the modern digital warehouse: AGVs, AMRs, and the full spectrum of Material Handling Vehicles (MHVs) - from forklifts and reach trucks to pallet trucks and tow tractors. Its compact, integrated design unifies a 2D SLAM LiDAR, a ceiling-forward vision sensor, and an IMU into a single, factory-calibrated unit.
At its heart lies our Fusion SLAM™ technology - a tightly-coupled fusion algorithm and a deep-learning engine honed through nearly ten years of real-world data accumulation and corner-case refinement. Forged by this experience, the system continuously evaluates and weights multi-sensor data in real time, adapting to environmental conditions to ensure reliable, uninterrupted operation. Through this intelligent, adaptive fusion of LiDAR point clouds, visual features, and IMU data, it consistently delivers stable ±3 cm accuracy at 10 Hz - all processed onboard.

## Key Applications

The V2 Pro is engineered for three core operational needs:
1)	The Core Positioning Device for AGVs & AMRs
The V2 Pro provides the centimeter-accurate, infrastructure-free positioning essential for Autonomous Guided Vehicles (AGVs) and Autonomous Mobile Robots (AMRs) to execute core tasks- such as material transport, facility inspection, and industrial cleaning - with full reliability.
2)	The Ideal Retrofit Kit for Manual-to-Autonomous Conversion
It serves as the complete positioning and navigation unit for transforming manual forklifts into autonomous AGVs. This enables rapid, cost-effective automation of existing assets.
3)	The Precision Awareness Device for Manual MHVs
For the broader spectrum of non-autonomous Material Handling Vehicles (MHVs) including reach trucks, pallet trucks, order pickers, tow tractors, and more, the V2 Pro provides high-precision real-time location data. This enables critical capabilities such as proximity safety alerts, accurate fleet tracking, and rich data feeds for digital twin systems, forming the intelligent sensory layer of the modern digital warehouse.

## Technical Specifications

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
## Documentation & Resources

| Resource                         | Link                                                                                                                  |
| -------------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| **HTTP Communication Protocol**  | [View Documentation](https://github.com/Lanxin-MRDVS/V2Pro-Kit/wiki/V2-Pro-HTTP-Communication-Protocol)                        |
| **UDP Communication Protocol**   | [View Documentation](https://github.com/Lanxin-MRDVS/V2Pro-Kit/wiki/V2-Pro-UDP-Communication-Protocol)                         |
| **ROS1 SDK Download**            | [Download SDK](https://github.com/Lanxin-MRDVS/V2Pro-Kit/releases/download/Firmware/V2_ROS_SDK.zip)                  |
| **ROS1 Interface Documentation** | [View Documentation](https://github.com/Lanxin-MRDVS/V2Pro-Kit/wiki/V2-Pro-ROS1-Interface)                                     |
| **ROS2 SDK Download**            | [Download SDK](https://github.com/Lanxin-MRDVS/V2Pro-Kit/releases/download/Firmware/lx_camera_ros2_ws.zip)           |
| **ROS2 Interface Documentation** | [View Documentation](https://github.com/Lanxin-MRDVS/V2Pro-Kit/wiki/V2-Pro-ROS2-Interface)                                     |
| **QR Code Tags**                 | [Download ZIP](https://github.com/Lanxin-MRDVS/V2Pro-Kit/releases/download/Firmware/V2Pro_QRcode_tags.zip)           |
| **Firmware Download**            | [Download Firmware](https://github.com/Lanxin-MRDVS/V2Pro-Kit/releases/download/Firmware/hontai_update_260318_V1.1.1.bin) |
