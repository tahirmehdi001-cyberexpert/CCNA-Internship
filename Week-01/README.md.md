# &#x20; Week 01 – CCNA Networking Internship



&#x20;**Organization:**  \[TechBiz Academy](https://academy.techbiz-sec.com/)  

&#x20;**Intern:**      Tahir Mehdi  

&#x20;**Student ID:**  TBS-2026-2582  

&#x20;**Program:**     CCNA Networking Internship



\---



## &#x20; **Week 1 – Task 1**



&#x20;**Build Your CCNA Lab + How Networks Actually Work**



&#x20;**Task Date:**  10 November 2026  

&#x20;**Submission Deadline:**  12 November 2026



&#x20;**Task Overview**



The objective of this task was to build a basic network topology using Cisco Packet Tracer and understand how computer networks communicate.



I created a network consisting of two routers, two switches, and four PCs. I configured IP addressing and routing to establish communication between different networks.



&#x20;
 **Network Topology**



&#x20;Devices Used: 



|**Device**|**Quantity**|
|-|-|
|Cisco Routers|2|
|Cisco Switches|2|
|PCs|4|





&#x20;**Network Design:** 



* &#x20;LAN 1: PC1, PC2, Switch 1 and Router 1
* &#x20;WAN Link: Router 1 connected to Router 2
* &#x20;LAN 2: PC3, PC4, Switch 2 and Router 2



&#x20;**IP Addressing**



| Device | Interface | IP Address |

|---|---|---|

| Router 1 | Serial 0/3/0 | 10.0.0.1 |

| Router 2 | Serial 0/3/0 | 10.0.0.2 |



The remaining LAN addressing and device configurations are documented in the lab report.



&#x20;**Practical Activities**



* &#x20;Created a network topology in Cisco Packet Tracer.
* &#x20;Connected routers using serial interfaces.
* &#x20;Configured IP addresses on router interfaces.
* &#x20;Configured switches and PCs.
* &#x20;Practiced routing between separate networks.
* &#x20;Tested connectivity using ICMP ping.
* &#x20;Used Cisco IOS verification commands.
* &#x20;Studied how packets travel between two hosts.



&#x20;**Commands Practiced**



```cisco

enable

configure terminal

interface serial 0/3/0

ip address 10.0.0.1 255.255.255.252

no shutdown

```



**Verification commands:**



```cisco

show ip interface brief

show ip route

show running-config

```

&#x20;**Network Packet Journey**



The packet travels from PC1 to PC4 through the following devices:



```text

PC1

&#x20;|

Switch 1

&#x20;|

Router 1

&#x20;|

Router 2

&#x20;|

Switch 2

&#x20;|

PC4

```



This helped me understand how switches forward frames and routers forward packets between different networks.



&#x20;**Screenshots**



**Network Topology**

!\[Network Topology](Screenshots\\Topology.png)





**Ping Connectivity Test**

!\[Ping Test on PC1](Screenshots/Ping-Test-On-PC1.png)

!\[Ping Test on PC4](Screenshots/Ping-Test-On-PC4.png)

&#x20;

**Show Ip Interface brief**

!\[Show Ip Interface brief Router 1](Screenshots/Show Ip interface breif-Roter 1.png)

!\[Show Ip Interface brief Router 2](Screenshots/Show Ip interface breif-Roter 2.png)



**Show ip Route**

!\[Show ip route of Router 1](Screenshots/Show ip route of Router 1.png)

!\[Show ip route of Router 2](Screenshots/Show ip route of Router 2.png)



Screenshots will be added after completing and verifying the practical lab.



**Files Included**



| File | Description |

|---|---|

| `Lab-Report.pdf` | Complete practical lab report |

| `Week1-Task1.pkt` | Cisco Packet Tracer project |

| `Screenshots/` | Practical configuration screenshots |



**Learning Outcomes**



Through this task, I improved my understanding of:



&#x20;Networking fundamentals

&#x20;Cisco Packet Tracer

&#x20;IP addressing and subnet masks

&#x20;Router and switch configuration

&#x20;Serial communication

&#x20;Network routing

&#x20;ICMP and ping testing

&#x20;Network troubleshooting



&#x20;**Conclusion**



This was my first practical task in the TechBiz Academy CCNA Networking Internship. It provided hands-on experience in designing a network topology, configuring Cisco devices, and understanding communication between different networks.



I look forward to completing more practical networking tasks and strengthening my CCNA skills.



\---



&#x20;**Intern:**  Tahir Mehdi  

&#x20;**Internship:**  TechBiz Academy – CCNA Networking  

&#x20;**Focus:**  Networking | Routing \& Switching | Cybersecurity

