# Campus Area Network (CAN) – Cisco Packet Tracer Project

![Cisco](https://img.shields.io/badge/Cisco-Packet%20Tracer-blue)
![OSPF](https://img.shields.io/badge/Routing-OSPF-orange)
![HSRP](https://img.shields.io/badge/Redundancy-HSRP-red)
![VLAN](https://img.shields.io/badge/Segmentation-VLANs-green)
![Security](https://img.shields.io/badge/Security-ACL%20%7C%20DAI%20%7C%20DHCP%20Snooping-purple)
![License](https://img.shields.io/badge/License-Academic-lightgrey)

## 📌 Overview

This project implements a **secure and scalable Campus Area Network (CAN)** using Cisco Packet Tracer.

The network follows a **three-tier architecture (Core – Distribution – Access)** and includes:

- VLAN segmentation
- Inter-VLAN routing
- OSPF dynamic routing
- HSRP redundancy
- Layer 2 security features
- Centralized network services (DHCP, DNS, NTP, Syslog, FTP)

The goal is to simulate a real enterprise campus network with high availability and security best practices.

---

## 🏗 Network Architecture

- 5 Routers
- 4 Layer 3 Switches
- 5 Layer 2 Switches
- Multiple VLANs (IT, HR, Sales, Healthcare, Management)
- Service DMZ
- Media DMZ

---

## 🔧 Technologies Used

- Cisco Packet Tracer
- OSPF (Area 0)
- HSRP
- STP
- VLANs
- ACLs
- DHCP Snooping
- Dynamic ARP Inspection
- Port Security
- SSH

---

## 🌐 VLAN Addressing

| VLAN       | Network         | Gateway      |
| ---------- | --------------- | ------------ |
| IT         | 192.168.10.0/24 | 192.168.10.1 |
| HR         | 192.168.20.0/24 | 192.168.20.1 |
| Sales      | 192.168.30.0/24 | 192.168.30.1 |
| Healthcare | 192.168.40.0/24 | 192.168.40.1 |
| Management | 192.168.50.0/24 | 192.168.50.1 |

Point-to-point links use /30 subnets.

---

## 🖥 Services Implemented

- DHCP Server (automatic IP assignment)
- DNS Server (name resolution)
- NTP Server (time synchronization)
- Syslog Server (centralized logging)
- FTP Server (file transfer)
- Email Server (internal communication)

---

## 🔐 Security Features

- ACLs for inter-VLAN filtering
- Port Security on access switches
- DHCP Snooping
- Dynamic ARP Inspection
- SSH for secure device access

---

# ▶ How to Run the Project

### 1️⃣ Requirements

- Install **Cisco Packet Tracer** (version 8.x recommended)

You can download it from:
[https://www.netacad.com](https://www.netacad.com) (requires free Cisco NetAcad account)

---

### 2️⃣ Open the Project

1. Launch Cisco Packet Tracer
2. Open the `.pkt` project file
3. Wait for devices to fully initialize

---

### 3️⃣ Verify the Network

You can test the implementation using:

#### ✅ Ping Test

From any PC:

```
ping 192.168.X.X
```

Test communication between VLANs.

#### ✅ HSRP Failover Test

- Shutdown active router interface:

```
interface g0/0
shutdown
```

- Verify standby router becomes active.

#### ✅ OSPF Verification

On routers:

```
show ip route
show ip ospf neighbor
```

#### ✅ DHCP Test

On a PC:

- Set IP configuration to DHCP
- Confirm IP is assigned automatically

#### ✅ DNS Test

From PC browser:

- Access configured domain name
- Verify name resolution works

---

# 📌 What This Project Demonstrates

- Enterprise VLAN segmentation
- Dynamic routing scalability
- Gateway redundancy
- Layer 2 security implementation
- Centralized service architecture
- Hierarchical campus design
