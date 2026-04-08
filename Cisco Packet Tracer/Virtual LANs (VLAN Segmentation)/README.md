### Project 5: Virtual LANs (VLAN Segmentation)

* **Goal:**
    * Split one physical Switch into two isolated virtual networks.
    * Ensure the **SALES** department cannot access the **HR** department for security.

* **What I did:**
    * **Created VLANs:** Defined two separate IDs on the Switch: `VLAN 10` (Sales) and `VLAN 20` (HR).
    * **Assigned Ports:** Locked specific Switch ports to their respective VLANs (Ports 1-5 for Sales, 6-10 for HR).
    * **Static Addressing:** Configured PCs with unique IP subnets for each department (`192.168.10.x` and `192.168.20.x`).
    * **Access Control:** Created a "virtual wall" — PCs in the same VLAN communicate, but crossing to another VLAN is blocked.

* **Key Results:**
    * **Security:** Successfully isolated sensitive HR data from the Sales department.
    * **Traffic Control:** Reduced broadcast traffic, improving network performance.
    * **Verification:** Used `show vlan brief` to confirm port assignments and verified with failed Pings between different departments.

* **Why it matters:**
    * VLANs are the foundation of **Cybersecurity** in any enterprise.
    * It allows managing thousands of users on the same hardware without mixing their data.

<img width=49% height="800" alt="image" src="https://github.com/user-attachments/assets/8e598820-8c89-4334-877d-4527850c1e72" />
<img width=49% height="800" alt="image" src="https://github.com/user-attachments/assets/b4ac253d-a5d8-4ce1-92dc-a73fa6efd9b3" />
<img width=49% height="800" alt="image" src="https://github.com/user-attachments/assets/325ec93f-53fe-417b-a8f9-e4775b985b51" />
