# 🌐 Types of Networks & Device Identification

## 🔗 Types of Networks
1. **Public Network** 🌍  
   - A large infrastructure that connects multiple private networks.  
   - Example: The **Internet**.  

2. **Private Network** 🏠  
   - Smaller, self-contained groups of devices.  
   - Example: Your **home Wi-Fi** or an **office LAN**.  

---

## 🖥️ Device Identification on a Network
Devices on a network are primarily recognized in **two ways**:

### 1. **IP Address** 🌍  
- An **IP address (Internet Protocol address)** temporarily identifies a device (host) on a network.  
- It allows data to be routed **to and from the correct device**.  
- IP addresses are not always fixed — they can change or be reassigned.  

#### 📌 Types of IP addresses:
- **Private IP address** – Used within local/internal networks (e.g., `192.168.x.x`).  
- **Public IP address** – Used when connecting to the broader Internet.  

---

### 2. **MAC Address** 🏷️  
- Every device has a **physical network interface** (like a Wi-Fi card or Ethernet port).  
- This interface is assigned a **MAC (Media Access Control) address** during manufacturing.  
- A MAC address is a **12-character hexadecimal number** (e.g., `38:FC:98:39:2A:15`).  

📌 Structure of a MAC address:  
- **First 6 characters (OUI)** – Identify the manufacturer.  
- **Last 6 characters** – Unique to the device, ensuring global uniqueness.  

---

## ⚙️ Additional Notes
- **NAT (Network Address Translation)** 🔄  
   - Allows multiple devices to share **one public IP address**.  
   - Example: All devices in your home share your ISP’s single public IP.  

- **Ping Command** 📡  
   - A basic networking tool using **ICMP (Internet Control Message Protocol)**.  
   - Sends an **Echo Request** and waits for an **Echo Reply**.  
   - Used to test connectivity and measure **round-trip time (RTT)**.  

---

