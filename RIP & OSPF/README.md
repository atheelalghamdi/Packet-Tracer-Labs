# RIP & OSPF Multi-Area with ISP Lab

This lab demonstrates a hybrid routing scenario combining **RIP v2** with **OSPF (Area 0 and Area 1)**, and includes an external connection to an **ISP router**.
The goal is to achieve full connectivity across RIP, OSPF, and ISP domains using **route redistribution**.

---

## 🎯 Objectives

- Configure dynamic routing using **RIP v2** and **OSPF multi-area**.
- Implement **redistribution** between RIP and OSPF for seamless route sharing.
- Ensure end-to-end connectivity between all LANs and the ISP network.
- Verify how external routes propagate across OSPF and RIP domains.

---

## 🖼️ Topology Overview

- **4 Routers**:
- **R1** → RIP domain (172.16.31.0/24).
- **ASBR2** → Border router connecting RIP with OSPF Area 1.
- **ASBR/ABR** → Core router between OSPF Area 1 and Area 0, also connected to ISP.
- **R0** → OSPF Area 0 router with LAN 172.16.30.0/24.
- **ISP Router** → Connected via Serial link (200.10.10.252/30).

- **Areas**:
- **Area 1**: between ASBR2 and ASBR/ABR.
- **Area 0 (Backbone)**: between ASBR/ABR and R0.


```bash

Kindly-Note: The first ICMP ping may fail due to initial ARP resolution and route setup. Subsequent pings should be successful.