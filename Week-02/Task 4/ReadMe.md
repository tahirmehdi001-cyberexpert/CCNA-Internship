# 🚀 CCNA Networking Internship — Week 2

<h3 align="center">Task 04: VLANs and Access Ports</h3>

<p align="center">
  <img src="https://img.shields.io/badge/Internship-TechBizAcademy-167C75?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Week-02-blue?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Task-04-orange?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Platform-Cisco%20Packet%20Tracer-049FD9?style=for-the-badge&logo=cisco" />
</p>

---

## 📌 Project Overview

This project demonstrates the configuration and implementation of **Virtual Local Area Networks (VLANs)** using a Cisco 2960 Layer 2 switch in Cisco Packet Tracer.

The lab focuses on network segmentation, access port assignment, broadcast domain isolation, MAC address learning, and connectivity testing between devices within the same VLAN and across different VLANs.

**The objective** is to understand how VLANs improve network organization, reduce unnecessary broadcast traffic, and provide logical separation between departments.

## 🎯 Lab Objectives

- Understand broadcast domains and the limitations of flat networks.
- Create and configure three VLANs.
- Assign switch access ports to their respective VLANs.
- Configure static IP addresses on end devices.
- Verify VLAN configuration using Cisco IOS commands.
- Examine the MAC address table.
- Test connectivity within and between VLANs.
- Demonstrate Layer 2 network isolation.

## 🖥️ Lab Environment

| Component | Specification |
|---|---|
| Simulation Tool | Cisco Packet Tracer |
| Switch | Cisco Catalyst 2960 |
| End Devices | 6 PCs |
| VLANs | 3 |
| Network Type | Layer 2 Switched Network |
| Cabling | Copper Straight-Through |
| IP Configuration | Static IPv4 |
| Routing | No Inter-VLAN Routing |

## 🗺️ Network Topology

The topology consists of one Cisco 2960 switch connected to six PCs, divided into three logical VLANs.

**Topology Design:**

```text
                  Cisco 2960 Switch
                         |
          +--------------+--------------+
          |              |              |
       VLAN 10         VLAN 20        VLAN 30
        STAFF          FINANCE         GUEST
          |              |              |
       +--+--+        +--+--+        +--+--+
       |     |        |     |        |     |
      PC0   PC1      PC2   PC3      PC4   PC5
     Fa0/1 Fa0/2    Fa0/3 Fa0/4    Fa0/5 Fa0/6
```

### 📸 Topology Screenshot

<!-- Insert your own Packet Tracer topology screenshot below -->

![VLAN Network Topology](screenshots/vlan-topology.png)

## 🏷️ VLAN Configuration Plan

| VLAN ID | VLAN Name | Purpose | Switch Ports |
|---|---|---|---|
| 10 | Staff | Staff Department | Fa0/1 – Fa0/2 |
| 20 | Finance | Finance Department | Fa0/3 – Fa0/4 |
| 30 | Guest | Guest Network | Fa0/5 – Fa0/6 |

## 🌐 IP Addressing Scheme

Each VLAN uses a separate IPv4 subnet.

| Device | VLAN | IP Address | Subnet Mask |
|---|---|---|---|
| Staff-PC1 | 10 | 192.168.10.11 | 255.255.255.0 |
| Staff-PC2 | 10 | 192.168.10.12 | 255.255.255.0 |
| Finance-PC1 | 20 | 192.168.20.11 | 255.255.255.0 |
| Finance-PC2 | 20 | 192.168.20.12 | 255.255.255.0 |
| Guest-PC1 | 30 | 192.168.30.11 | 255.255.255.0 |
| Guest-PC2 | 30 | 192.168.30.12 | 255.255.255.0 |

## ⚙️ Cisco IOS Configuration

### 1. Create VLANs

```bash
enable
configure terminal

vlan 10
 name Staff
exit

vlan 20
 name Finance
exit

vlan 30
 name Guest
exit
```

### 2. Assign Access Ports

**Staff VLAN — VLAN 10**

```bash
interface range fa0/1-2
 switchport mode access
 switchport access vlan 10
exit
```

**Finance VLAN — VLAN 20**

```bash
interface range fa0/3-4
 switchport mode access
 switchport access vlan 20
exit
```

**Guest VLAN — VLAN 30**

```bash
interface range fa0/5-6
 switchport mode access
 switchport access vlan 30
exit
```

### 3. Save Configuration

```bash
end
write memory
```

## 🔍 Verification Commands

The following commands were used to verify the switch configuration.

| Command | Purpose |
|---|---|
| `show vlan brief` | Verify VLANs and assigned ports |
| `show mac address-table` | View learned MAC addresses |
| `show running-config` | Display the running switch configuration |
| `show mac address-table vlan 10` | Display MAC entries for VLAN 10 |
| `show mac address-table vlan 20` | Display MAC entries for VLAN 20 |
| `show mac address-table vlan 30` | Display MAC entries for VLAN 30 |

### VLAN Verification

<!-- Insert your own show vlan brief screenshot -->

![VLAN Verification](screenshots/vlan-verification.png)

### MAC Address Table Verification

<!-- Insert your own show mac address-table screenshot -->

![MAC Address Table](screenshots/mac-address-table.png)

## 🧪 Connectivity Testing

Connectivity was tested to verify communication within the same VLAN and isolation between different VLANs.

### Same-VLAN Connectivity

| Source | Destination | Expected Result | Status |
|---|---|---|---|
| Staff-PC1 | Staff-PC2 | Successful | PASS |
| Finance-PC1 | Finance-PC2 | Successful | PASS |
| Guest-PC1 | Guest-PC2 | Successful | PASS |

**Example Ping Command:**

```bash
ping 192.168.10.12
```

### 📸 Successful Ping Evidence

<!-- Insert your own successful ping screenshots -->

**VLAN 10 — Staff**

![Staff VLAN Ping](screenshots/staff-ping.png)

**VLAN 20 — Finance**

![Finance VLAN Ping](screenshots/finance-ping.png)

**VLAN 30 — Guest**

![Guest VLAN Ping](screenshots/guest-ping.png)

### Cross-VLAN Connectivity

| Source | Destination | Expected Result | Status |
|---|---|---|---|
| Staff-PC1 | Finance-PC1 | Failed | PASS |
| Staff-PC1 | Guest-PC1 | Failed | PASS |
| Finance-PC1 | Guest-PC2 | Failed | PASS |

**Example Ping Command:**

```bash
ping 192.168.20.11
```

### 📸 Failed Ping Evidence

<!-- Insert your own failed ping screenshots -->

![Staff to Finance Isolation](screenshots/staff-finance-failed-ping.png)

![Finance to Guest Isolation](screenshots/finance-guest-failed-ping.png)

![Guest to Finance Isolation](screenshots/guest-finance-failed-ping.png)

## 📊 Results and Observations

- Successfully created three VLANs: Staff, Finance, and Guest.
- Assigned all six access ports to their respective VLANs.
- Configured static IPv4 addresses for all PCs.
- Verified VLAN membership using `show vlan brief`.
- Examined dynamically learned MAC addresses using `show mac address-table`.
- Confirmed successful communication between PCs within the same VLAN.
- Verified isolation between different VLANs without inter-VLAN routing.

## 🎓 Key Learning Outcomes

Through this practical lab, I gained hands-on experience with:

- VLAN creation and management.
- Access port configuration.
- Layer 2 network segmentation.
- Broadcast domain separation.
- Static IPv4 configuration.
- MAC address learning and switching.
- Cisco IOS verification commands.
- Network connectivity troubleshooting.

## 🛠️ Tools & Technologies

<p>
  <img src="https://img.shields.io/badge/Cisco-Packet%20Tracer-049FD9?style=flat-square&logo=cisco" />
  <img src="https://img.shields.io/badge/Networking-VLANs-167C75?style=flat-square" />
  <img src="https://img.shields.io/badge/IPv4-Addressing-blue?style=flat-square" />
  <img src="https://img.shields.io/badge/CLI-Cisco%20IOS-black?style=flat-square" />
</p>
## 📥 Download PDF Report

You can view or download the complete documentation of this VLAN configuration lab.

| Resource | Description |
|---|---|
| 📄 [Download PDF Report](docs\Week2_Task4_Report.pdf) | Complete Week 2 – Task 4 lab report |
| 👁️ [View PDF Report](docs\Week2_Task4_Report.pdf) | Open the report directly from GitHub |

**Report includes:**
- VLAN configuration and IP addressing
- Cisco IOS configuration commands
- VLAN verification screenshots
- MAC address table verification
- Same-VLAN connectivity tests
- Inter-VLAN isolation tests
- Results, observations, and conclusion

> **Note:** Make sure the PDF is uploaded to the `report` folder in your GitHub repository using this exact filename: `TechBizAcademy-Week-2-Task-4.pdf`.


## 👨‍💻 Internship Information

| Detail | Information |
|---|---|
| Intern | Tahir Mehdi |
| Organization | TechBizAcademy |
| Student ID | TBS-2026-2582 |
| Internship | CCNA Networking Internship |
| Week | Week 2 |
| Task | Task 4 — VLANs and Access Ports |
| Lab Platform | Cisco Packet Tracer |

## 📌 Conclusion

This practical lab provided hands-on experience in configuring VLANs and access ports on a Cisco Layer 2 switch. The implementation successfully demonstrated logical network segmentation, MAC address learning, and communication within individual VLANs.

The connectivity tests demonstrated that devices in different VLANs remain isolated when inter-VLAN routing is not configured.

---

<p align="center">
  <b>CCNA Networking Internship — Week 2, Task 4</b><br/>
  <i>Learn • Configure • Verify • Practice</i>
</p>

<p align="center">
  Made with dedication by <b>Tahir Mehdi</b>
</p>