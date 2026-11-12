

# &#x20;🌐 IPv4 Addressing \& Subnetting | Week 1 – Task 2



<p align="center">

&#x20; <img src="https://img.shields.io/badge/TechBiz%20Academy-Networking%20Internship-blue?style=for-the-badge" />

&#x20; <img src="https://img.shields.io/badge/Task-Week%201%20%7C%20Task%202-success?style=for-the-badge" />

&#x20; <img src="https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge" />

</p>



<p align="center">

&#x20; <b>Practical Implementation of IPv4 Addressing, Binary Conversion \& VLSM Subnetting</b>

</p>



\---



## \## 👨‍💻 Student Information



&#x20;

| **Detail**|**Information** |
|-|-|
|**Name**|Tahir Mehdi|
|**Student ID**|TBS-2026-2582|
|**Organization**|TechBiz Academy|
|**Internship Task**|Week 1 – Task 2|
|**Task Title**|IPv4 Addressing and Subnetting |
|**Maximum Score**|10 Quality Points |
|**Submission Date**|14 November 2026|





\---



### \## 🎯 Project Overview



This task focuses on understanding and implementing fundamental IPv4 networking concepts through theoretical calculations and practical Cisco Packet Tracer configuration.



The main objective was to divide the network `192.168.10.0/24` into five subnets using \*\*Variable Length Subnet Masking (VLSM)\*\* and apply the addressing plan to the existing Week 1 Task 1 network topology.



\### 📌 Learning Objectives



* &#x20;Understand IPv4 addressing and 32-bit binary representation.
* &#x20;Convert decimal values into 8-bit binary.
* &#x20;Understand subnet masks and CIDR prefix notation.
* &#x20;Identify network addresses, broadcast addresses and usable host ranges.
* &#x20;Perform VLSM subnet calculations.
* &#x20;Configure router and PC IPv4 addresses.
* &#x20;Verify network connectivity using ICMP ping commands.



\---



### \## 🧠 Topics Covered



&#x20;

|                                    **Topic**|                                     **Description** |
|-|-|
|**IPv4 Addressing**|32-bit addressing structure|
|**Binary Conversion**|Decimal to binary conversion|
|**Subnet Mask** |Network and host portions |
|**CIDR**|Prefix length notation|
|**VLSM**|Variable Length Subnet Masking|
|**Packet Tracer** |Practical network configuration|
|**Connectivity Testing**|Gateway and PC-to-PC ping tests|



\---



### \## 🔢 VLSM Subnetting Plan



**Given Network:** `192.168.10.0/24`



**Host Requirements:**  50, 25, 12, 2 and 2 hosts.



The subnets were allocated from the largest host requirement to the smallest to use IP address space efficiently.

|      **Subnet**|     **Required Hosts**|     **Network / CIDR**|          **Subnet Mask**|        **Usable Hosts**|
|-|-|-|-|-|
|A|50|192.168.10.0/26|255.255.255.192|62|
|B|25|192.168.10.64/27|255.255.255.224|30 |
|C|12|192.168.10.96/28|255.255.255.240|14|
|D|2|192.168.10.112/30|255.255.255.252|2|
|E|2|192.168.10.116/30|255.255.255.252|2|



### \### 📍 Detailed Address Allocation



|                      **Subnet**|                  **Usable Host Range** |                  **Broadcast Address** |
|-|-|-|
|A|192.168.10.1 – 192.168.10.62|192.168.10.63|
|B|192.168.10.65 – 192.168.10.94|192.168.10.95|
|C|192.168.10.97 – 192.168.10.110|192.168.10.111|
|D|192.168.10.113 – 192.168.10.114|192.168.10.115|
|E|192.168.10.117 – 192.168.10.118|192.168.10.119|



\---



### \## 🖥️ Practical Lab – Cisco Packet Tracer



The VLSM addressing plan was applied to the Week 1 Task 1 topology.



#### \### Network Topology



* &#x20;2 Cisco Routers
* &#x20;2 Network Switches
* &#x20;4 End Devices (PCs)
* &#x20;Router-to-Router connection
* &#x20;Two separate LAN networks



#### \### IP Addressing Configuration

&#x20;

|               **Device**|            **IP Address**|           **Subnet Mask**|             **Default Gateway**|
|-|-|-|-|
| Router 1 – LAN|192.168.10.1|255.255.255.192|-|
|PC1|192.168.10.2|255.255.255.192|192.168.10.1|
|PC2|192.168.10.2|255.255.255.192|192.168.10.1|
|Router 2 – LAN|192.168.10.65|255.255.255.224|-|
|PC1|192.168.10.66|255.255.255.224|192.168.10.65|
|PC2|192.168.10.67|255.255.255.224|192.168.10.65|
|Router 1 – Serial|192.168.10.113|255.255.255.252|-|
|Router 2 – Serial|192.168.10.114|255.255.255.252|-|





\---



### \## 🧪 Connectivity Verification



Connectivity was checked using Cisco Packet Tracer command-line tools.



#### \### Commands Used



```bash

show ip interface brief

show running-config

show ip route

ipconfig

ping <destination-IP>

```



#### \### Connectivity Tests



|                      **Test**|                       **Source**|                     **Destination**|
|-|-|-|
|Gateway Ping|PC1|192.168.10.1|
|Gateway Ping |PC3|192.168.10.65|
| Neighbour Ping|PC1|192.168.10.3|
|Inter-Network Ping|PC1|192.168.10.67|



\---



### \## 📸 Practical Evidence



Screenshots from the Packet Tracer lab are included in the internship task report.



| Screenshot | Description |

|---|---|

| 01 | Complete Packet Tracer Network Topology |

| 02 | Router 1 \& Router 2 – Interface Configuration |

| 03 | PC IP Configuration |

| 04 | Gateway Ping Verification |

| 05 | Neighbour PC Ping |

| 06 | Inter-Network Ping |



📄 \*\*Full Task Report:\*\*  

`Week\_1\_Task\_2\_IPv4\_Subnetting\_Report\_Tahir\_Mehdi.pdf`



\---



### \## 📚 Key Learnings



Through this task, I improved my understanding of:



* &#x20;IPv4 addressing and binary calculations.
* &#x20;Subnetting and efficient IP address allocation.
* &#x20;VLSM design based on host requirements.
* &#x20;Router and end-device IP configuration.
* &#x20;Network connectivity troubleshooting.
* &#x20;Practical networking using Cisco Packet Tracer.



\---



\## 🚀 Tools \& Technologies



<p>

&#x20; <img src="https://img.shields.io/badge/Cisco-Packet%20Tracer-1BA0D7?style=flat-square\&logo=cisco\&logoColor=white" />

&#x20; <img src="https://img.shields.io/badge/IPv4-Networking-blue?style=flat-square" />

&#x20; <img src="https://img.shields.io/badge/VLSM-Subnetting-green?style=flat-square" />

</p>



\---



<p align="center">

&#x20; <b>TechBiz Academy – Networking Internship</b><br>

&#x20; Week 1 | Task 2 – IPv4 Addressing and Subnetting<br><br>

&#x20; <i>Learning by configuring, testing and troubleshooting networks.</i>

</p>



