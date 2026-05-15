# Network Infrastructure & Connectivity Lab | SoftUni Exam

This repository contains the completed configuration for a comprehensive networking lab exam. The project demonstrates proficiency in multi-router static routing, VLAN management, Spanning Tree Protocol (STP) optimization, and essential network services (DNS/HTTPS).

## 📌 Project Overview
The primary goal was to establish full end-to-end connectivity in a complex topology, ensuring that client devices (Laptops) in different VLANs can access secure web resources across multiple routed segments.

### Key Objectives:
* **Inter-VLAN Routing:** Implement "Router-on-a-Stick" to allow communication between isolated client segments.
* **Static Routing:** Configure explicit hop-by-hop routing without using default gateways on routers.
* **STP Load Balancing:** Configure Rapid PVST+ with specific Root Bridge priorities to optimize traffic flow.
* **Service Hardening:** Enable DNS resolution and enforce secure HTTPS protocols while disabling insecure HTTP.

## 🛠 Technology Stack
* **Routing:** Static Routing (Next-hop concept), Sub-interfaces (802.1Q).
* **Switching:** VLANs (101, 102), Trunking, Rapid PVST+.
* **Services:** DNS, HTTPs, ICMP.
* **Platform:** Cisco Packet Tracer.

## 🌐 Network Design & Addressing

### IP Schema
The network is segmented into several subnets to simulate a real-world enterprise environment:
| Segment | Subnet | Key Devices |
| :--- | :--- | :--- |
| **VLAN 101** | `10.1.101.0/24` | Laptop1, Laptop3 |
| **VLAN 102** | `10.1.102.0/24` | Laptop2, Laptop4 |
| **Inter-Router** | `10.0.1.0/28`, `10.0.2.0/28` | R1, R2, R3 |
| **Server Farm 1** | `192.168.1.0/24` | WEB Server 1 |
| **Server Farm 2** | `192.168.2.0/24` | DNS Server |
| **Server Farm 3** | `192.168.3.0/24` | WEB Server 2 |

### Spanning Tree Protocol (STP) Configuration
To ensure path redundancy and efficiency, **Rapid PVST+** was implemented with the following logic:
* **Switch2:** Primary Root Bridge for **VLAN 101** (configured with the second-lowest priority).
* **Switch3:** Primary Root Bridge for **VLAN 102** (configured with the second-lowest priority).

## 🚀 Implementation Steps

1.  **Interface Management:** Enabled all administratively down interfaces via CLI and assigned hostnames (R1, R2, R3, SW1-SW4).
2.  **L3 Configuration:** Configured physical interfaces and sub-interfaces (encapsulation dot1Q) for inter-VLAN routing on Router1.
3.  **Static Routing:** Populated routing tables on R1, R2, and R3 using explicit next-hop addresses. Verified that no "Gateway of Last Resort" was used.
4.  **VLAN & Trunking:** Created VLANs 101/102 across all switches and configured inter-switch links as Trunks.
5.  **Service Activation:** * Activated the **DNS Service** to resolve `www.softuni1.bg` and `www.softuni2.bg`.
    * Enabled **HTTPS** and disabled **HTTP** on both Web Servers for security compliance.
    * Configured DNS server IPs on all client Laptops.

## 🔍 Verification
The lab was successfully verified through:
- **Ping Tests:** End-to-end reachability between all subnets.
- **DNS Resolution:** Laptops successfully resolve server hostnames.
- **Web Access:** Successful browser connection to `https://www.softuni1.bg` from all clients.
- **STP State:** Verified Root Bridge placement using `show spanning-tree`.

---
*This project was completed as part of the SoftUni Networking Curriculum.*

<img width=49% height="600" alt="image" src="https://github.com/user-attachments/assets/266a5342-f536-4582-b2c8-a3a7fd994922" />
