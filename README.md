📘 RIP–OSPF Redistribution & ISP NAT Lab
🔹 Overview

This lab demonstrates integrating RIP v2 and OSPF Multi-Area routing protocols, configuring special OSPF areas (Stub, Totally Stub, NSSA), using redistribution, and providing ISP connectivity via NAT.

The project showcases advanced routing, redistribution, and verification techniques, simulating a real-world enterprise-to-ISP connection.

🔹 Topology

🔹 Key Features

✅ RIP v2 configuration for edge networks

✅ OSPF Multi-Area deployment (normal, stub, totally stub, NSSA)

✅ Virtual Link to maintain backbone continuity

✅ Redistribution between RIP and OSPF domains

✅ Default Route Injection for external connectivity

✅ NAT at R1 for ISP access

✅ End-to-End Reachability verification with ping & traceroute

🔹 Verification

show ip ospf database → confirmed LSAs & backbone design

show ip route → validated redistribution between RIP & OSPF

ping & traceroute → tested end-to-end reachability to ISP (90.0.0.1, 50.0.0.2)

NAT translation confirmed with debug ip nat

🔹 Lessons Learned

How different OSPF area types (Stub, Totally Stub, NSSA) affect LSA propagation

Importance of virtual links when backbone rules are broken

Role of default routes & redistribution in reachability

NAT ACL design — avoid including external/ISP subnets

Using verification commands effectively in troubleshooting

🔹 Repository Structure
RIP-OSPF-Redistribution-Lab/
│── README.md        # Project overview (this file)
│── report.md        # Full detailed report with configs & explanations
│── configs/         # Per-router configurations (R1.txt, R2.txt, ...)
│── screenshots/     # Verification outputs (OSPF DB, routing table, pings)
│── topology.png     # Network topology diagram
