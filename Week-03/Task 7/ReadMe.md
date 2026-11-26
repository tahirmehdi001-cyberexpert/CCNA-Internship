# Week 3 – Task 7: Static and Default Routing

![Cisco Packet Tracer](https://img.shields.io/badge/Cisco-Packet%20Tracer-blue?logo=cisco)
![CCNA](https://img.shields.io/badge/Networking-CCNA-red)
![Status](https://img.shields.io/badge/Status-Completed-success)

## Project Overview

This project was completed as part of the **CCNA Networking Internship at TechBiz Academy**.

The objective of this lab was to configure and understand IPv4 Static Routing and Default Routing using Cisco Packet Tracer. The practical work demonstrates how routers forward packets between multiple LAN networks using manually configured routes.

## Lab Objectives

- Configure IPv4 static routes between different LAN networks.
- Configure default routes (Gateway of Last Resort).
- Understand routing tables using `show ip route`.
- Configure router interfaces and IP addressing.
- Verify end-to-end connectivity between multiple LANs.
- Understand Administrative Distance and route selection.

## Network Topology

The lab consists of:

- 3 Routers (R1, R2, R3)
- 3 Switches
- 6 End Devices (PCs)
- 3 LAN Networks
- 2 Serial Point-to-Point Links

### IP Addressing Scheme

| Network | IP Address |
|---|---|
| LAN 1 | 192.168.10.0/24 |
| LAN 2 | 192.168.20.0/24 |
| LAN 3 | 192.168.30.0/24 |
| R1 – R2 | 10.0.12.0/30 |
| R2 – R3 | 10.0.23.0/30 |

## Practical Labs

### 1. Static Routing

Configured static routes to establish communication between three different LAN networks.

**Key configurations:**
- Static route configuration using `ip route`.
- Next-hop address configuration.
- Routing table analysis.
- Floating static route concepts.
- Administrative Distance (AD).

**Packet Tracer File:**

[Download Static Routing Lab](Static_routing.pkt)

### 2. Default Routing

Configured default routes to forward unknown destination traffic toward the central router (R2).

**Key configurations:**
- Default route: `0.0.0.0 0.0.0.0`
- Gateway of Last Resort.
- Static routes on the central router.
- Default route verification.
- End-to-end connectivity testing.

**Packet Tracer File:**

[Download Default Routing Lab](Default_Static_Routing.pkt)

## Verification Commands

```bash
show ip route
show ip route static
show ip interface brief
show ip route 0.0.0.0
ping 192.168.20.2
ping 192.168.30.2
```

## Results

- Successfully configured static routes.
- Configured default routes on R1 and R3.
- Verified routing tables on all three routers.
- Successfully tested communication between different LAN networks.
- Achieved successful ping responses with 0% packet loss in the documented connectivity tests.

## Technologies & Skills

- Cisco Packet Tracer
- IPv4 Addressing
- Static Routing
- Default Routing
- Floating Static Routing
- Administrative Distance
- Routing Table Analysis
- Network Troubleshooting
- End-to-End Connectivity Testing

## Documentation

The complete practical report, including configurations, routing table outputs, verification screenshots, and results, is available below.

📄 [View Week 3 – Task 7 Report](docs/Week_3_Task_7_Static_and_Default_Routing_Report.pdf)

---

## Internship Information

**Organization:** TechBiz Academy  
**Program:** CCNA Networking Internship  
**Intern:** Tahir Mehdi  
**Student ID:** TBS-2026-2582  
**Task:** Week 3 – Task 7  
**Topic:** Static and Default Routing

---

*Hands-on networking practice | Learning by configuring, testing, and troubleshooting.*