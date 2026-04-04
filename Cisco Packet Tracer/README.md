## Project 1: Peer-to-Peer (P2P) Connection
**Date:** April 4, 2026
**Tool:** Cisco Packet Tracer

### Task Description:
The goal was to establish a direct physical and logical connection between two host computers and verify connectivity.

### Implementation Steps:
* **Hardware:** Added two Generic PCs to the workspace.
* **Cabling:** Used a **Copper Cross-Over** cable to connect the FastEthernet0 interfaces (required for direct connection between similar devices).
* **IP Addressing:** * **PC0:** `192.168.1.1` (Subnet Mask: `255.255.255.0`)
  * **PC1:** `192.168.1.2` (Subnet Mask: `255.255.255.0`)

### Verification:
I successfully verified the connection by using the `ping` command from PC0 to PC1.

**Command Output:**
```text
Pinging 192.168.1.1 with 32 bytes of data:

Reply from 192.168.1.1: bytes=32 time=6ms TTL=128
Reply from 192.168.1.1: bytes=32 time=2ms TTL=128
Reply from 192.168.1.1: bytes=32 time<1ms TTL=128
Reply from 192.168.1.1: bytes=32 time=4ms TTL=128

Ping statistics for 192.168.1.1:
    Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),
Approximate round trip times in milli-seconds:
    Minimum = 0ms, Maximum = 6ms, Average = 3ms
```
<img width="872" height="885" alt="image" src="https://github.com/user-attachments/assets/85d55804-bddf-43e8-9c80-20eec9ff7276" />
