# Project #4: DHCP Server Automation (Dynamic IP)

### **Goal:**
* **Eliminate manual IP entry** for every computer in the network.
* **Configure a Cisco Router** to assign network settings automatically using DHCP.

---

### 🛠 **Step-by-Step Implementation:**

* **1. Gateway & Interface Setup**
    * Assigned fixed IP addresses to the Router's physical ports to act as **Default Gateways**.
    * Fixed the **"Unassigned Interface"** error by properly assigning IP `192.168.1.1`.
    * Activated ports using the **`no shutdown`** command (changed status from Red to **Green**).

* **2. DHCP Pool Configuration**
    * Created virtual "reservoirs" of IP addresses for each office: **OFFICE_A** and **OFFICE_B**.
    * Defined the **Network range** and the **Default Router** (Gateway) for each pool.

* **3. Final Automation**
    * Switched all PCs from **Static** to **DHCP** mode in the settings.
    * All computers instantly received their **IP, Subnet Mask, and Gateway** from the Router.

---

### ✅ **Results:**
* **Dynamic Assignment:** PCs successfully received IP addresses (e.g., `192.168.1.2`) automatically.
* **Troubleshooting:** Resolved the **APIPA (169.254.x.x)** issue by fixing the Router's interface status.
* **Connectivity:** Verified successful **Ping** communication between different office subnets.

---

<img width=49% height="800" alt="image" src="https://github.com/user-attachments/assets/31278e14-f3b0-4712-ab08-0d15fafc8da6" />
<img width=49% height="800" alt="image" src="https://github.com/user-attachments/assets/7443fd76-2753-4215-9263-560edfbae1de" />
<img width=49% height="800" alt="image" src="https://github.com/user-attachments/assets/21b7aec3-47ff-4bb0-928e-5b8507ac97ed" />


