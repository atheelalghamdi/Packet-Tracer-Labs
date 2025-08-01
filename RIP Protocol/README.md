# RIP Routing Lab

This lab demonstrates a network topology that uses **RIP v2 (Routing Information Protocol)** for dynamic routing between multiple LAN segments distributed across two routers.

## 🧠 Objective

- Configure dynamic routing using RIP v2 across R1 and R2.
- Achieve full connectivity between 6 different subnets.
- Understand the behavior of RIP in a multi-router environment.
- Observe automatic route propagation without manual static routes.

## 🗺️ Topology Overview

- **2 Routers** (R1, R2) connected to a simulated ISP.
- **6 LANs**, each connected via its own switch.
- **Subnetting** using `/26` and `/24` ranges for better IP management.
- **End devices (PC0 to PC5)** configured with appropriate IPs and gateways.

## ⚙️ Configuration Highlights

- RIP enabled with:
```bash
router rip
version 2
no auto-summary
network 192.168.0.0
network 172.16.31.0
network 172.17.32.0

Kindly-Note: The first ICMP ping may fail due to initial ARP resolution and route setup. Subsequent pings should be successful.
