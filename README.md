# Cisco RIP Configuration in Packet Tracer

This repository contains a project demonstrating how to configure **Routing Information Protocol (RIP) v2** in Cisco Packet Tracer.

## 📌 Project Overview
This project includes:
- Configuring **RIP v2** on three routers.
- Connecting **three different networks** using RIP.
- Verifying connectivity using the **`ping`** command.

## 🛠️ Network Topology
![Network Topology](image.png)

## 🚀 Configuration Steps

### **1️⃣ Router 0 (R0)**
```bash
interface FastEthernet 0/0
 ip address 192.168.1.1 255.255.255.0
 no shutdown
!
interface FastEthernet 0/1
 ip address 10.0.0.1 255.255.255.252
 no shutdown
!
router rip
 version 2
 network 192.168.1.0
 network 10.0.0.0
 no auto-summary
Router 1
interface FastEthernet 0/0
 ip address 192.168.3.1 255.255.255.0
 no shutdown
!
interface Ethernet 1/0
 ip address 10.0.0.2 255.255.255.252
 no shutdown
!
interface FastEthernet 0/1
 ip address 10.0.1.2 255.255.255.252
 no shutdown
!
router rip
 version 2
 network 192.168.3.0
 network 10.0.0.0
 network 10.0.1.0
 no auto-summary
Router 2
interface FastEthernet 0/0
 ip address 192.168.2.1 255.255.255.0
 no shutdown
!
interface FastEthernet 0/1
 ip address 10.0.1.1 255.255.255.252
 no shutdown
!
router rip
 version 2
 network 192.168.2.0
 network 10.0.1.0
 no auto-summary

