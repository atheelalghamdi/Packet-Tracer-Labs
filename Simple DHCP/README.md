

# DHCP Lab – Automatic IP Addressing in a LAN

This simple lab demonstrates the configuration and behavior of **DHCP (Dynamic Host Configuration Protocol)** using a single router as the DHCP server for a small LAN.

## 🎯 Objective

- Configure a Cisco router to act as a **DHCP server**.
- Automatically assign IP addresses to multiple end devices.
- Verify successful IP assignment and connectivity across the network.

## 🗺️ Topology Overview

- **1 Router**
- **1 Switch**
- **4 PCs** connected to the switch

## ⚙️ Configuration Summary

### DHCP Settings on Router:

```bash
ip dhcp pool atheel
network 192.168.10.0 255.255.255.0
default-router 192.168.10.1
dns-server 8.8.8.8

ip dhcp excluded-address 192.168.10.1 

interface GigabitEthernet0/0
ip address 192.168.10.1 255.255.255.0
no shutdown

Kindly-Note: The first ICMP ping may fail due to initial ARP resolution and route setup. Subsequent pings should be successful.
