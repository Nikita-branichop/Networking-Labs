# Project 07: Inter-VLAN Routing with Standard ACL Security

## Description
This project demonstrates the implementation of a secure network infrastructure using a **Router-on-a-Stick** topology in Cisco Packet Tracer. The main goal was to segment the network into two distinct VLANs (Managers and Guests) and enforce security policies using **Standard Access Control Lists (ACLs)**.

## Network Topology
* **Router (2911):** Acting as the default gateway for all VLANs using sub-interfaces.
* **Switch (2960):** Handles VLAN segmentation and trunking.
* **VLAN 10 (Managers):** Subnet `192.168.10.0/24` (Includes PC-Manager and Admin-Server).
* **VLAN 20 (Guests):** Subnet `192.168.20.0/24` (Includes PC-Guest).

## Key Features Implemented
1.  **VLAN Segmentation:** Created and named VLANs to isolate department traffic.
2.  **Router-on-a-Stick:** Configured 802.1Q encapsulation on router sub-interfaces (`G0/0.10`, `G0/0.20`).
3.  **Traffic Filtering (ACL):** * Implemented a **Standard ACL** to protect the Manager's network.
    * Configured the ACL to **deny** all traffic from the Guest subnet (`192.168.20.0/24`) to the Manager subnet.
    * Permitted all other traffic (e.g., to external networks/Internet).
4.  **Trunking:** Configured IEEE 802.1Q trunking between the switch and the router.

## Verification Results
* **PC-Manager to Admin-Server:** Successful (Intra-VLAN communication).
* **PC-Manager to PC-Guest:** Successful (Inter-VLAN routing working).
* **PC-Guest to Admin-Server:** **Failed** (Correctly blocked by ACL).
* **PC-Guest to Gateway:** Successful (Verification that the interface is up).

## How to Run
1. Open the `.pkt` file in **Cisco Packet Tracer**.
2. Wait for the STP (Spanning Tree Protocol) to converge (green lights).
3. Use the **Simple PDU tool** or **Command Prompt** to verify the connectivity and security rules.

---
*Status: Completed as part of SysAdmin-PET-projects series.*

<img width=49% height="800" alt="image" src="https://github.com/user-attachments/assets/19f47ca8-f1c0-4426-a3e6-c4b0bb4dd60a" />
<img width=49% height="800" alt="image" src="https://github.com/user-attachments/assets/b9b985c7-48c2-4588-aca8-42b2b8f7a820" />
<img width=49% height="800" alt="image" src="https://github.com/user-attachments/assets/6923df0d-fd35-442e-85e4-83552cf7ddec" />
