# 🌐 IPv4 Addressing & Subnetting | Week 1 – Task 2

<p align="center">
  <img src="https://img.shields.io/badge/TechBiz%20Academy-Networking%20Internship-blue?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Week-01-orange?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Task-02-success?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Cisco-Packet%20Tracer-1BA0D7?style=for-the-badge&logo=cisco&logoColor=white" />
</p>

**Practical Implementation of IPv4 Addressing, Binary Conversion & VLSM Subnetting**

---

## 👨‍💻 Student Information

| Detail | Information |
|:---|:---|
| **Name** | Tahir Mehdi |
| **Student ID** | TBS-2026-2582 |
| **Organization** | TechBiz Academy |
| **Internship** | Networking Internship |
| **Task** | Week 1 – Task 2 |
| **Maximum Score** | 10 Quality Points |
| **Submission Date** | 14 November 2026 |

---

## 🎯 Project Overview

This project demonstrates the practical implementation of fundamental IPv4 networking concepts, including binary conversion, subnet masks, CIDR notation, and Variable Length Subnet Masking (VLSM).

The primary objective was to divide the network **192.168.10.0/24** into five smaller subnets based on different host requirements and implement the addressing plan using Cisco Packet Tracer.

The practical implementation was performed using the network topology created in Week 1 – Task 1.

## 📌 Learning Objectives

- Understand IPv4 addressing and its 32-bit binary structure.
- Convert decimal values into 8-bit binary.
- Understand subnet masks and CIDR notation.
- Calculate network addresses and broadcast addresses.
- Identify usable host ranges.
- Perform VLSM subnet calculations.
- Configure router and PC IPv4 addresses.
- Verify network connectivity using ICMP ping.

---

## 🧠 Topics Covered

| Topic | Description |
|:---|:---|
| IPv4 Addressing | 32-bit addressing structure |
| Binary Conversion | Decimal to binary conversion |
| Subnet Mask | Network and host portions |
| CIDR | Prefix length notation |
| VLSM | Variable Length Subnet Masking |
| Packet Tracer | Practical network configuration |
| Connectivity Testing | Gateway and PC-to-PC ping tests |

---

## 🔢 VLSM Subnetting Plan

**Given Network:** `192.168.10.0/24`

**Host Requirements:** 50, 25, 12, 2 and 2 hosts.

Subnets were allocated from the largest host requirement to the smallest to ensure efficient utilization of the available IP address space.

| Subnet | Required Hosts | Network / CIDR | Subnet Mask | Usable Hosts |
|:---:|---:|:---|:---|---:|
| A | 50 | `192.168.10.0/26` | `255.255.255.192` | 62 |
| B | 25 | `192.168.10.64/27` | `255.255.255.224` | 30 |
| C | 12 | `192.168.10.96/28` | `255.255.255.240` | 14 |
| D | 2 | `192.168.10.112/30` | `255.255.255.252` | 2 |
| E | 2 | `192.168.10.116/30` | `255.255.255.252` | 2 |

### 📍 Detailed Address Allocation

| Subnet | Usable Host Range | Broadcast Address |
|:---:|:---|:---|
| A | `192.168.10.1 – 192.168.10.62` | `192.168.10.63` |
| B | `192.168.10.65 – 192.168.10.94` | `192.168.10.95` |
| C | `192.168.10.97 – 192.168.10.110` | `192.168.10.111` |
| D | `192.168.10.113 – 192.168.10.114` | `192.168.10.115` |
| E | `192.168.10.117 – 192.168.10.118` | `192.168.10.119` |

---

## 🖥️ Practical Implementation – Cisco Packet Tracer

The calculated VLSM addressing scheme was applied to the existing Week 1 – Task 1 network topology.

### Network Topology Components

- 2 Cisco Routers
- 2 Network Switches
- 4 End Devices (PCs)
- Router-to-Router Serial Connection
- Two Separate LAN Networks

### 🌐 Network Topology

The following screenshot shows the complete network topology implemented in Cisco Packet Tracer.

![Complete Network Topology](screenshots/01-topology.png)

---

## ⚙️ IP Addressing Configuration

The following IP addressing scheme was configured on the routers and end devices.

| Device | IP Address | Subnet Mask | Default Gateway |
|:---|:---|:---|:---|
| Router 1 – LAN | `192.168.10.1` | `255.255.255.192` | — |
| PC1 | `192.168.10.2` | `255.255.255.192` | `192.168.10.1` |
| PC2 | `192.168.10.3` | `255.255.255.192` | `192.168.10.1` |
| Router 2 – LAN | `192.168.10.65` | `255.255.255.224` | — |
| PC3 | `192.168.10.66` | `255.255.255.224` | `192.168.10.65` |
| PC4 | `192.168.10.67` | `255.255.255.224` | `192.168.10.65` |
| Router 1 – Serial | `192.168.10.113` | `255.255.255.252` | — |
| Router 2 – Serial | `192.168.10.114` | `255.255.255.252` | — |

### Router Interface Verification

**Router 1 – Show IP Interface Brief**

![Router 1 Interface Verification](screenshots/02-router1-show-ip-interface-brief.png)

**Router 2 – Show IP Interface Brief**

![Router 2 Interface Verification](screenshots/03-router2-show-ip-interface-brief.png)

### PC IP Configuration

**PC1 – IP Configuration**

![PC1 IP Configuration](screenshots/04-pc1-ip-configuration.png)

**PC4 – IP Configuration**

![PC4 IP Configuration](screenshots/05-pc4-ip-configuration.png)

---

## 🧪 Connectivity Verification

Connectivity was tested using Cisco Packet Tracer command-line tools to verify communication between gateways, neighboring PCs, and separate LAN networks.

### Commands Used

```bash
show ip interface brief
show running-config
show ip route
ipconfig
ping <destination-IP>
```

### Connectivity Testing Results

| Test | Source | Destination | Expected Result |
|:---|:---|:---|:---|
| Gateway Ping | PC1 | `192.168.10.1` | Successful |
| Gateway Ping | PC3 | `192.168.10.65` | Successful |
| Neighbour Ping | PC1 | `192.168.10.3` | Successful |
| Inter-Network Ping | PC1 | `192.168.10.67` | Successful |

### 1. Gateway Connectivity – PC1 to Router 1

![PC1 to Router 1 Successful Ping](screenshots/06-gateway-ping-pc1-router1.png)

### 2. Gateway Connectivity – PC3 to Router 2

![PC3 to Router 2 Successful Ping](screenshots/07-gateway-ping-pc3-router2.png)

### 3. Neighbour Connectivity – PC1 to PC2

![PC1 to PC2 Successful Ping](screenshots/08-neighbour-ping-pc1-pc2.png)

### 4. Inter-Network Connectivity – PC1 to PC4

![PC1 to PC4 Successful Ping](screenshots/09-inter-network-ping-pc1-pc4.png)

---

## 📸 Practical Evidence Summary

All practical configurations and connectivity tests were performed in Cisco Packet Tracer.

| No. | Screenshot |
|:---:|:---|
| 01 | Complete Network Topology |
| 02 | Router 1 – Show IP Interface Brief |
| 03 | Router 2 – Show IP Interface Brief |
| 04 | PC1 – IP Configuration |
| 05 | PC4 – IP Configuration |
| 06 | Gateway Ping – PC1 to Router 1 |
| 07 | Gateway Ping – PC3 to Router 2 |
| 08 | Neighbour Ping – PC1 to PC2 |
| 09 | Inter-Network Ping – PC1 to PC4 |

---

## 📄 Full Task Report

For detailed calculations, explanations, and practical evidence, refer to the complete PDF report:

**[Week 1 – Task 2: IPv4 Addressing & Subnetting Report](docs/Week_1_Task_2_IPv4_Subnetting_Report_Tahir_Mehdi.pdf)**

---

## 📚 Key Learnings

Through this practical task, I strengthened my understanding of:

- IPv4 addressing and binary calculations.
- Subnetting and efficient IP address allocation.
- VLSM subnet design based on host requirements.
- Router and end-device IP configuration.
- Network connectivity testing and troubleshooting.
- Practical networking using Cisco Packet Tracer.

---

## 🛠️ Tools & Technologies

<p>
  <img src="https://img.shields.io/badge/Cisco-Packet%20Tracer-1BA0D7?style=flat-square&logo=cisco&logoColor=white" />
  <img src="https://img.shields.io/badge/IPv4-Networking-blue?style=flat-square" />
  <img src="https://img.shields.io/badge/VLSM-Subnetting-green?style=flat-square" />
  <img src="https://img.shields.io/badge/Cisco-IOS-lightgrey?style=flat-square&logo=cisco" />
  <img src="https://img.shields.io/badge/GitHub-Version%20Control-black?style=flat-square&logo=github" />
</p>

---

## 🚀 Internship Progress

**TechBiz Academy – Networking Internship**

| Week | Task | Status |
|:---:|:---|:---:|
| Week 1 | Task 1 – Network Topology | Completed |
| Week 1 | Task 2 – IPv4 Addressing & Subnetting | Completed |

---

<p align="center">
  **Learning by Configuring, Testing & Troubleshooting Networks.**
  
  <br/>
  Developed by **Tahir Mehdi**
</p>