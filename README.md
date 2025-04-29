# 🏦 Banking Network Simulation (Cisco Packet Tracer)

This project is a simulation of a multi-floor banking network infrastructure built using Cisco Packet Tracer. It demonstrates VLAN segmentation, DHCP automation, wireless access, inter-VLAN communication, routing with OSPF, server deployment, and security policies.

---

## 📋 Project Objectives

- Implement **OSPF** as the routing protocol.
- Support up to **60 users** per department with both **wired and wireless** access.
- All clients must obtain IP addresses via **DHCP**.
- Enable communication between departments using **inter-VLAN routing**.
- Configure an **HTTP server** and an **Email server**.
- All IP addresses are assigned **dynamically from the Layer 3 switch**.
- Enable **SSH access** on all routers.
- Apply **basic configuration** on all devices:
  - Hostname
  - Enable & Console Passwords
  - Message of the Day Banner
  - Disable DNS Lookup
  - Password Encryption
- Each department is isolated in its own **VLAN and subnet**.
- Apply **Port Security**:
  - Sticky MAC addresses
  - Violation mode: shutdown
- **Verify** full end-to-end communication across the network.

---

Here is the visual representation of the topology:

---

## 🧠 IP Addressing & VLAN Plan

| VLAN | Department       | Subnet               | Subnet Mask       | Usable IP Range          | Broadcast Address    |
|------|------------------|----------------------|--------------------|---------------------------|-----------------------|
| 10   | Management       | 192.168.10.0/27      | 255.255.255.224    | 192.168.10.1 – .30        | 192.168.10.31         |
| 20   | Research         | 192.168.10.32/27     | 255.255.255.224    | 192.168.10.33 – .62       | 192.168.10.63         |
| 30   | HR               | 192.168.10.64/27     | 255.255.255.224    | 192.168.10.65 – .94       | 192.168.10.95         |
| 40   | Marketing        | 192.168.10.96/27     | 255.255.255.224    | 192.168.10.97 – .126      | 192.168.10.127        |
| 50   | Accounting       | 192.168.10.128/27    | 255.255.255.224    | 192.168.10.129 – .158     | 192.168.10.159        |
| 60   | Finance          | 192.168.10.160/27    | 255.255.255.224    | 192.168.10.161 – .190     | 192.168.10.191        |
| 70   | Logistics        | 192.168.10.192/27    | 255.255.255.224    | 192.168.10.193 – .222     | 192.168.10.223        |
| 80   | Customer Care    | 192.168.10.224/27    | 255.255.255.224    | 192.168.10.225 – .254     | 192.168.10.255        |
| 90   | Guest            | 192.168.11.0/26      | 255.255.255.192    | 192.168.11.1 – .62        | 192.168.11.63         |
| 100  | Administration   | 192.168.11.64/27     | 255.255.255.224    | 192.168.11.65 – .94       | 192.168.11.95         |
| 110  | ICT              | 192.168.11.96/27     | 255.255.255.224    | 192.168.11.97 – .126      | 192.168.11.127        |
| 120  | Server Room      | 192.168.11.128/29    | 255.255.255.248    | 192.168.11.129 – .134     | 192.168.11.135        |

---

## ⚙️ Configuration Highlights

### Routers
- OSPF routing enabled
- SSH configured for secure remote login
- Hostname, banners, passwords, and security settings applied

### Layer 3 Switch
- Serves as **DHCP Server** for all VLANs
- Routes between VLANs
- Configured with **SVIs** for each VLAN
- Configured VTP Server

### Switches (Access Layer)
- VLANs assigned to access ports
- Port Security enabled (Sticky MAC, Violation Shutdown)

### Wireless Access Points
- Deployed in each department for wireless users

### Servers
- **HTTP Server** for web services
- **Email Server** for internal communication

---

## 🔒 Security Features

- SSH on routers
- Encrypted passwords
- Port security (MAC binding and shutdown)
- Access control through VLANs

---

## ✅ Testing & Verification

- DHCP leasing confirmed
- Inter-VLAN communication verified
- SSH access successful
- HTTP and Email services operational

---

## 📁 Included Files

- `banking-network.pkt` (Packet Tracer file)
