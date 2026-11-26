# Week 3 – Task 8: OSPFv2 Single-Area

## CCNA Networking Internship | TechBiz Academy

This task focuses on configuring, verifying, and troubleshooting **OSPFv2 (Open Shortest Path First)** in a multi-router network using Cisco Packet Tracer.

### 🎯 Objectives

- Configure OSPFv2 using Process ID 10 and Area 0.
- Configure explicit OSPF Router IDs.
- Establish and verify OSPF neighbour adjacencies.
- Configure passive interfaces for LAN-facing ports.
- Troubleshoot OSPF Hello/Dead timer mismatches.
- Modify OSPF interface cost to influence route selection.
- Verify routing paths using traceroute and routing tables.

### 🌐 Network Topology

The lab uses three Cisco routers (R1, R2, R3), three LAN networks, switches, and six PCs.

| Device | IP Address / Network |
|---|---|
| R1 LAN | 192.168.10.0/24 |
| R2 LAN | 192.168.20.0/24 |
| R3 LAN | 192.168.30.0/24 |
| R1–R2 | 10.0.12.0/30 |
| R2–R3 | 10.0.23.0/30 |

### ⚙️ Technologies & Concepts

- Cisco IOS CLI
- OSPFv2
- Single-Area OSPF (Area 0)
- Router IDs
- Passive Interfaces
- OSPF Neighbour Adjacency
- Hello/Dead Timers
- OSPF Interface Cost
- Route Selection
- Traceroute

### 🔧 Key Configurations

**OSPF Configuration (R1)**

```cisco
router ospf 10
 router-id 1.1.1.1
 network 10.0.12.0 0.0.0.3 area 0
 network 192.168.10.0 0.0.0.255 area 0
 passive-interface fastethernet 0/0
```

**OSPF Neighbour Verification**

```cisco
show ip ospf neighbor
show ip ospf interface brief
show ip route ospf
show ip protocols
```

**Hello/Dead Timer Troubleshooting**

```cisco
interface serial 0/3/0
 ip ospf hello-interval 5
 ip ospf dead-interval 20
```

Restore default timers:

```cisco
interface serial 0/3/0
 no ip ospf hello-interval
 no ip ospf dead-interval
```

**OSPF Cost Modification**

```cisco
interface serial 0/3/1
 ip ospf cost 200
```

### 🧪 Practical Results

- Successfully configured OSPFv2 with Process ID 10 and Area 0.
- Verified FULL neighbour adjacency between routers.
- Demonstrated adjacency failure caused by mismatched Hello/Dead timers.
- Restored adjacency by correcting timer values.
- Modified OSPF interface cost to influence route selection.
- Verified the selected route through next-hop `10.0.12.2`.
- Confirmed an OSPF metric of `129`.
- Successfully tested end-to-end connectivity using `tracert`.

### 📥 Download Project Files

Access the practical report and Cisco Packet Tracer lab file below.

| Resource | Download |
|---|---|
| 📄 Practical Report (PDF) | [Download Report](docs/Week_3_Task_8_OSPFv2_Report.pdf) |
| 🌐 Packet Tracer Lab (.pkt) | [Download Packet Tracer File](./OSPFv2_Single-Area.pkt) |

**Files Included:**
- Complete OSPFv2 configuration and practical documentation.
- Cisco Packet Tracer topology with router configurations.
- Neighbour verification and troubleshooting evidence.
- OSPF cost modification and route selection testing.

### 🛠️ Software Used

- Cisco Packet Tracer 9.0
- Cisco IOS CLI

### 👨‍💻 Internship Information

| Detail | Information |
|---|---|
| Intern | Tahir Mehdi |
| Student ID | TBS-2026-2582 |
| Organization | TechBiz Academy |
| Program | CCNA Networking Internship |
| Week | Week 3 |
| Task | Task 8 – OSPFv2 Single-Area |

### 📌 Learning Outcome

This practical strengthened my understanding of dynamic routing, OSPF neighbour formation, routing table analysis, timer troubleshooting, and metric-based path selection in Cisco networking environments.

---

**Author:** Tahir Mehdi  
**GitHub:** [@tahirmehdi001-cyberexpert](https://github.com/tahirmehdi001-cyberexpert)

*Learning • Configuring • Troubleshooting • Securing Networks*