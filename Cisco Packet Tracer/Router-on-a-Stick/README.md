# Project 6: Inter-VLAN Routing (Router-on-a-Stick)

## Description
In this project, I configured communication between two isolated VLANs using a single physical link between a Cisco Router and a Switch. This method is known as "Router-on-a-Stick".

## Network Topology
- **VLAN 10 (Sales):** Subnet 192.168.10.0/24
- **VLAN 20 (HR):** Subnet 192.168.20.0/24
- **Router Interface:** Sub-interfaces with 802.1Q encapsulation.

## Key Concepts Applied
- **IEEE 802.1Q:** Tagging protocol used to identify VLANs on the trunk link.
- **Sub-interfaces:** Creating logical interfaces on a single physical router port.
- **Default Gateway:** Setting up the router as the gateway for different subnets to allow inter-network communication.

## Configuration Highlights (Router)
```bash
interface GigabitEthernet0/0.10
 encapsulation dot1Q 10
 ip address 192.168.10.254 255.255.255.0

interface GigabitEthernet0/0.20
 encapsulation dot1Q 20
 ip address 192.168.20.254 255.255.255.0
```

<img width=49% height="800" alt="image" src="https://github.com/user-attachments/assets/cb669502-93b8-4b1f-990b-49412a3fad28" />
<img width=49% height="800" alt="image" src="https://github.com/user-attachments/assets/27883f9c-a2e3-4054-99d8-d5f0a3cbee09" />
