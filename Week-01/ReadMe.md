# 🚀 CCNA Networking Internship — Week 1
### TechBiz Security | Networking & Infrastructure Labs

<p align="center">
  <img src="https://img.shields.io/badge/Internship-CCNA%20Networking-blue?style=for-the-badge&logo=cisco" />
  <img src="https://img.shields.io/badge/Organization-TechBiz%20Security-0A7B83?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Week-01-purple?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Status-Completed-success?style=for-the-badge" />
</p>

Welcome to my **Week 1 CCNA Networking Internship Portfolio** at **TechBiz Security**.

This repository documents my hands-on networking practice, Cisco Packet Tracer labs, IPv4 addressing, subnetting, Cisco IOS configuration, SSH implementation, and router password recovery.

The objective of Week 1 was to establish a strong foundation in computer networking and develop practical skills using Cisco networking technologies.

---

## 📌 Week 1 Overview

| Task | Title | Status | Score |
|---|---|---|---|
| Task 01 | Build Your CCNA Lab & How Networks Actually Work | ✅ Completed | 10/10 |
| Task 02 | IPv4 Addressing & Subnetting | ✅ Completed | 10/10 |
| Task 03 | The IOS Command Line, Interfaces & Recovery | ✅ Completed | 10/10 |

**Total confirmed score: 30/30** 

---

## 🧪 Task 01 — Build Your CCNA Lab & Networking Fundamentals

<details>
<summary><strong>📂 View Task 01 Documentation</strong></summary>

### 🎯 Objectives

- Install and configure Cisco Packet Tracer.
- Understand basic networking concepts and communication.
- Build a network topology containing:
  - 2 Routers
  - 2 Switches
  - 4 End Devices (PCs)
- Configure IP addresses on network devices.
- Establish communication between all four PCs.
- Understand the journey of a packet across a network.

### 🛠️ Technologies & Tools

- Cisco Packet Tracer
- Cisco Routers and Switches
- IPv4 Addressing
- ICMP / Ping
- Basic Network Topology

### 📸 Lab Evidence

**Network Topology**

![Task 01 Network Topology](screenshots/task-01/topology.png)

**PC Connectivity Verification**

![Task 01 Ping Test](screenshots/task-01/ping-test.png)

### 📁 Lab Files

- [Packet Tracer Lab](labs/task-01/)

### 🏆 Result

**10/10 — Excellent**

Successfully built the network topology and verified connectivity between all four PCs.

</details>

---

## 🧪 Task 02 — IPv4 Addressing & Subnetting

<details>
<summary><strong>📂 View Task 02 Documentation</strong></summary>

### 🎯 Objectives

- Understand IPv4 addressing and binary conversion.
- Convert decimal IPv4 octets into binary and vice versa.
- Understand subnet masks and CIDR notation.
- Identify network addresses and broadcast addresses.
- Calculate usable host ranges.
- Implement Variable Length Subnet Masking (VLSM).
- Re-address the existing Week 1 network topology.
- Verify connectivity using ping tests.

### 🛠️ Technologies & Concepts

- IPv4 Addressing
- Binary Conversion
- Subnet Masks
- CIDR Notation
- VLSM Subnetting
- Network Address Calculation
- Broadcast Address Calculation
- ICMP Connectivity Testing

### 📊 VLSM Requirements

The network `192.168.10.0/24` was divided to accommodate:

| Network Requirement | Required Hosts |
|---|---:|
| Subnet 01 | 50 |
| Subnet 02 | 25 |
| Subnet 03 | 12 |
| Subnet 04 | 2 |
| Subnet 05 | 2 |

### 📸 Lab Evidence

**Updated Network Topology**

![Task 02 Topology](screenshots/task-02/topology.png)

**IP Address Configuration**

![Task 02 IP Configuration](screenshots/task-02/ip-configuration.png)

**Connectivity Verification**

![Task 02 Ping Verification](screenshots/task-02/ping-test.png)

### 📁 Lab Files

- [Packet Tracer Lab](labs/task-02/)

### 🏆 Result

**10/10 — Excellent**

Successfully completed IPv4 subnetting exercises, implemented VLSM addressing, and verified network connectivity.

</details>

---

## 🧪 Task 03 — The IOS Command Line, Interfaces & Recovery

<details>
<summary><strong>📂 View Task 03 Documentation</strong></summary>

### 🎯 Objectives

- Understand Cisco IOS command-line interface (CLI).
- Work with User EXEC, Privileged EXEC and Global Configuration modes.
- Configure hostnames, banners and device passwords.
- Configure SSH for secure remote device management.
- Configure router and switch interfaces.
- Understand and execute essential Cisco IOS show commands.
- Save running configurations to startup configurations.
- Perform router password recovery using the configuration register.

### 🛠️ Technologies & Commands

| Command / Technology | Purpose |
|---|---|
| `enable` | Enter Privileged EXEC mode |
| `configure terminal` | Enter Global Configuration mode |
| `hostname` | Configure device hostname |
| `enable secret` | Secure privileged access |
| `banner motd` | Configure login warning banner |
| `username` | Create a local user account |
| `ip domain-name` | Configure domain name for SSH |
| `crypto key generate rsa` | Generate RSA keys |
| `ip ssh version 2` | Enable SSH version 2 |
| `show running-config` | Display active configuration |
| `show ip interface brief` | Display interface status and IP addresses |
| `show version` | Display IOS and device information |
| `copy running-config startup-config` | Save configuration |
| Configuration Register | Support router password recovery |

### 📸 Lab Evidence

**Router Configuration**

![Router Configuration](screenshots/task-03/router-configuration.png)

**Switch Configuration**

![Switch Configuration](screenshots/task-03/switch-configuration.png)

**SSH Verification**

![SSH Verification](screenshots/task-03/ssh-verification.png)

**Show Command Outputs**

![Show Commands](screenshots/task-03/show-commands.png)

**Password Recovery / Configuration Register**

![Password Recovery](screenshots/task-03/password-recovery.png)

**Post-Recovery Login Verification**

![Post Recovery Verification](screenshots/task-03/post-recovery-verification.png)

### 📁 Lab Files

- [Packet Tracer Lab](labs/task-03/)

### 🏆 Result

**Completed — Grading pending.**

Successfully practised Cisco IOS device configuration, secure remote access, configuration management and router password recovery.

</details>

---

## 🧠 Skills Developed During Week 1

| Category | Skills |
|---|---|
| Networking Fundamentals | Network Topologies, Devices, Packet Flow |
| Cisco Technologies | Cisco IOS, CLI, Router & Switch Configuration |
| IP Networking | IPv4, Binary Conversion, CIDR |
| Subnetting | VLSM, Network & Broadcast Calculation |
| Network Security | SSH, Passwords, Login Banners |
| Troubleshooting | Ping, Interface Verification, Show Commands |
| Configuration Management | Running & Startup Configuration |
| Recovery | Configuration Register & Password Recovery |

---

## 🧰 Tools & Technologies

<p>
  <img src="https://img.shields.io/badge/Cisco-Packet%20Tracer-049fd9?style=flat-square&logo=cisco&logoColor=white" />
  <img src="https://img.shields.io/badge/Cisco-IOS-blue?style=flat-square&logo=cisco" />
  <img src="https://img.shields.io/badge/Networking-IPv4-green?style=flat-square" />
  <img src="https://img.shields.io/badge/Protocol-SSH-orange?style=flat-square" />
  <img src="https://img.shields.io/badge/Protocol-ICMP-purple?style=flat-square" />
</p>

---

## 📈 Week 1 Learning Outcomes

By completing Week 1, I gained practical experience in:

1. Building and configuring a multi-device network topology.
2. Understanding how devices communicate across networks.
3. Performing IPv4 subnetting and VLSM calculations.
4. Configuring Cisco routers and switches through IOS CLI.
5. Implementing secure SSH remote management.
6. Verifying network interfaces and device configurations.
7. Saving configurations and performing router password recovery.

---

## 📂 Repository Structure

```text
Week-01/
│
├── README.md
│
├── Task 1/
│   ├── Task1.pkt
│   │   
│   ├── screenshots/
│   ├── README.md
    └── docs/
│
├── Task 2/
│   ├── docs/
│   │   └── Week_1_Task_2_IPv4_Subnetting_Report_Tahir_Mehdi.pdf
│   │── screenshots/
    ├── ReadMe.md
│   └── Week_1_Task_2_IPv4_Subnetting_Tahir_Mehdi.pkt
│
└── Task 03/
    ├── docs/
    │   └── Week1-Task3_Report.pdf
    ├── Packet-Tracer/
                  └──Week-1-Task-3-Lab.pkt
    ├── screenshots/
    └── ReadMe
```

---

## 👨‍💻 Author

**Tahir Mehdi**

ADP Computer Science Student | CCNA Networking Intern | Aspiring Network & Cybersecurity Professional

- **Organization:** TechBiz Security
- **Focus Areas:** Computer Networking, Network Security, Cisco Technologies and Cybersecurity
- **GitHub:** [Tahir Mehdi](https://github.com/tahirmehdi001-cyberexpert)
- **LinkedIn:** [Connect with me](https://www.linkedin.com/in/tahirmehdi18/)

---

<p align="center">
  <strong>WEEK 1 — SUCCESSFULLY COMPLETED 🚀</strong>
  <br/>
  Building strong networking foundations, one lab at a time.
  <br/><br/>
  <em>Hands-on Practice • Continuous Learning • Professional Growth</em>
</p>
