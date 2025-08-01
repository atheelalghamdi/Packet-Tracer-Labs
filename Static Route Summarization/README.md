# Static & Summary Routing Lab

This lab demonstrates static and summary routing across four LANs and an ISP connection using Cisco Packet Tracer.

## 🧠 Objectives:
- Configure and verify static routes.
- Implement route summarization between routers.
- Understand point-to-point serial links.
- Assign appropriate IP addresses and gateways to PCs.

## 🗺️ Topology Overview:
- **LAN1**: 173.16.64.0/23
- **LAN2**: 173.16.66.0/23
- **LAN3**: 173.16.68.0/24
- **LAN4**: 173.16.69.0/24
- **WAN links**:
- R1–R2: 173.16.71.4/30
- R1–ISP: 209.165.201.0/30

## ⚙️ Configuration Summary:
1. Configured LANs and interfaces.
2. On **Router R2**:
- Added summary route to LAN3 & LAN4.
- Added static route to ISP.
3. On **Router R1**:
- Added summary route to LAN1 & LAN2.
4. On **Router ISP**:
- Added summary route to all internal networks.
5. Configured PCs with static IPs and correct gateways.

## 📁 Files Included:
- `summary-routing-lab.pkt` – Packet Tracer project file.
- `topology-screenshot.png` – Visual reference of the network topology.
- `README.md` – Lab overview and documentation (this file).

## 🔧 Tools Used:
- Cisco Packet Tracer (Latest version)

```bash

Kindly-Note: The first ICMP ping may fail due to initial ARP resolution and route setup. Subsequent pings should be successful.
