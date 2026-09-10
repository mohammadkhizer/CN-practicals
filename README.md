# 🌐 Computer Networks Laboratory Practicals

Comprehensive collection of Cisco Packet Tracer simulation files (`.pkt`) and detailed lab documentations (`.pdf`) for the **Computer Networks Laboratory** course.

---

## 📌 Table of Contents

- [Overview](#-overview)
- [Prerequisites](#-prerequisites)
- [Repository Layout](#-repository-layout)
- [Detailed Practical Breakdown](#-detailed-practical-breakdown)
  - [Practical 1: Basic LAN Implementation using Network Switch](#practical-1-basic-lan-implementation-using-network-switch)
  - [Practical 2: Inter-Subnet Communication using Switches & Routers (Static Routing & DHCP)](#practical-2-inter-subnet-communication-using-switches--routers-static-routing--dhcp)
  - [Practical 3: Multi-Router Dynamic Routing (OSPF) & Hardware Modularity (WIC-2T)](#practical-3-multi-router-dynamic-routing-ospf--hardware-modularity-wic-2t)
  - [Practical 4: Advanced Subnetting (VLSM /27) & Multi-Router Static Routing Tables](#practical-4-advanced-subnetting-vlsm-27--multi-router-static-routing-tables)
  - [Practical 5: Integrated Multi-Network Topology Simulation](#practical-5-integrated-multi-network-topology-simulation)
- [How to Run Simulations](#-how-to-run-simulations)

---

## ℹ️ Overview

* **Author:** Shaikh Mohammed Khizer  
* **Enrollment:** `25CS501D053`  
* **Simulator:** Cisco Packet Tracer (v5.1 / v8.0+)  
* **Topics Covered:** LAN Topologies, Switch & Router Configuration, Static & Dynamic (OSPF) Routing, DHCP Pools, Subnetting (VLSM /27), WIC-2T Hardware Modules, ICMP Packet Verification.

---

## 🛠 Prerequisites

To open, edit, and simulate the network topology files:
* **Cisco Packet Tracer** (v8.0+ recommended; compatible with v5.1+)
* PDF Reader for inspecting original lab instructions in the [`PDF/`](file:///d:/GIT/CN-practicals/PDF) folder.

---

## 📁 Repository Layout

```
CN-practicals/
├── PDF/
│   ├── CN-PRACTICAL-1 .pdf    # Detailed lab guide for Practical 1
│   ├── CN-PRACTICAL-2.pdf     # Detailed lab guide for Practical 2
│   ├── CN-PRACTICAL-3.pdf     # Detailed lab guide for Practical 3
│   └── CN-PRACTICAL-4.pdf     # Detailed lab guide for Practical 4
├── prac-1.pkt                 # Packet Tracer simulation for Practical 1
├── prac-2.pkt                 # Packet Tracer simulation for Practical 2
├── prac-3.pkt                 # Packet Tracer simulation for Practical 3
├── prac-4.pkt                 # Packet Tracer simulation for Practical 4
├── prac-5.pkt                 # Packet Tracer simulation for Practical 5
├── screen-shots/              # Topology & verification screenshots
├── .gitignore                 # Ignored patterns (screenshots, binaries)
└── README.md                  # Main repository documentation
```

---

## 📘 Detailed Practical Breakdown

---

### Practical 1: Basic LAN Implementation using Network Switch
* **File:** [`prac-1.pkt`](file:///d:/GIT/CN-practicals/prac-1.pkt) | **Lab Manual:** [`CN-PRACTICAL-1 .pdf`](file:///d:/GIT/CN-practicals/PDF/CN-PRACTICAL-1%20.pdf)
* **Aim:** To implement a Local Area Network (LAN) using a network switch in Cisco Packet Tracer.

#### 📐 Topology & Devices
* **End Devices:** 3 PCs (`PC0`, `PC1`, `PC2`)
* **Intermediate Device:** 1 Network Switch (Cisco 2950-24)
* **Cabling:** Copper Straight-Through Cables

#### ⚙️ Configuration Details
1. Connect PCs to switch FastEthernet interfaces (`Fa0/1`, `Fa0/2`, `Fa0/3`).
2. Assign static IP addresses to all PCs on the same subnet:
   - **IP Range:** `192.168.100.2` – `192.168.100.4`
   - **Subnet Mask:** `255.255.255.0` (`/24`)
   - **Default Gateway:** `192.168.100.1`

#### 🧪 Testing & Verification
* Send Simple PDUs (ICMP Packets) from `PC0` (Source) to `PC2` (Destination).
* Verify **Successful** delivery status in the Packet Tracer Realtime/Simulation panel.

---

### Practical 2: Inter-Subnet Communication using Switches & Routers (Static Routing & DHCP)
* **File:** [`prac-2.pkt`](file:///d:/GIT/CN-practicals/prac-2.pkt) | **Lab Manual:** [`CN-PRACTICAL-2.pdf`](file:///d:/GIT/CN-practicals/PDF/CN-PRACTICAL-2.pdf)
* **Aim:** To implement a multi-network topology connecting two distinct LAN subnets via switches and routers.

#### 📐 Topology & Devices
* **Subnet 1 (`192.168.100.0/24`):** 3 PCs, 1 Switch (`Switch0`), 1 Server (`Server1`), 1 Router (`Router1`).
* **Subnet 2 (`192.168.200.0/24`):** 3 PCs, 1 Switch (`Switch1`), 1 Server (`Server2`), 1 Router (`Router2`).
* **WAN Link:** Router-to-Router connection over Serial link (`10.0.0.0/30`).

#### ⚙️ CLI Configuration Highlights

```cisco
! Router1 Configuration (Network 1 Side)
hostname Router1
interface FastEthernet0/0
 ip address 192.168.100.1 255.255.255.0
 no shutdown
exit

interface Serial0/0/0
 ip address 10.0.0.1 255.255.255.252
 clock rate 64000
 no shutdown
exit

! DHCP Pool Setup
ip dhcp excluded-address 192.168.100.1
ip dhcp excluded-address 192.168.100.254
ip dhcp pool NETWORK1
 network 192.168.100.0 255.255.255.0
 default-router 192.168.100.1
exit

! Static Route to reach Network 2
ip route 192.168.200.0 255.255.255.0 10.0.0.2
```

```cisco
! Router2 Configuration (Network 2 Side)
hostname Router2
interface FastEthernet0/0
 ip address 192.168.200.1 255.255.255.0
 no shutdown
exit

interface Serial0/0/0
 ip address 10.0.0.2 255.255.255.252
 no shutdown
exit

! DHCP Pool Setup
ip dhcp excluded-address 192.168.200.1
ip dhcp excluded-address 192.168.200.254
ip dhcp pool NETWORK2
 network 192.168.200.0 255.255.255.0
 default-router 192.168.200.1
exit

! Static Route to reach Network 1
ip route 192.168.100.0 255.255.255.0 10.0.0.1
```

#### 🧪 Testing & Verification
* Configure PCs to receive dynamic IP configuration via DHCP.
* Transmit PDUs across subnets (`Server1` to `PC3`).
* *Note:* The initial packet may show **Failed** due to ARP resolution; subsequent attempts result in **Successful** transmission.

---

### Practical 3: Multi-Router Dynamic Routing (OSPF) & Hardware Modularity (WIC-2T)
* **File:** [`prac-3.pkt`](file:///d:/GIT/CN-practicals/prac-3.pkt) | **Lab Manual:** [`CN-PRACTICAL-3.pdf`](file:///d:/GIT/CN-practicals/PDF/CN-PRACTICAL-3.pdf)
* **Aim:** To construct a topology with 3+ routers utilizing OSPF dynamic routing protocol and WIC-2T WAN interface expansion modules.

#### 📐 Topology & Hardware Expansion
* **Hardware Expansion:** Power down Cisco 1841 routers and install **WIC-2T** (2-port Serial WAN Interface Cards) to enable multi-point WAN interconnections.
* **3 Network Subnets:**
  - `LAN 1`: `192.168.10.0/24` (Gateway: `192.168.10.1`)
  - `LAN 2`: `192.168.20.0/24` (Gateway: `192.168.20.1`)
  - `LAN 3`: `192.168.30.0/24` (Gateway: `192.168.30.1`)
* **Serial Point-to-Point WAN Links:** `192.168.100.0/30`, `192.168.100.4/30`, `192.168.100.8/30`.

#### ⚙️ Key OSPF Configuration (Sample for Router0)

```cisco
router ospf 1
 network 192.168.10.0 0.0.0.255 area 0
 network 192.168.100.0 0.0.0.3 area 0
 network 192.168.100.4 0.0.0.3 area 0
exit
```

#### 🧪 Testing & Verification
* OSPF dynamically discovers routes across all 3 routers.
* Verify end-to-end connectivity across all subnets using Packet Tracer's PDU tool.

---

### Practical 4: Advanced Subnetting (VLSM /27) & Multi-Router Static Routing Tables
* **File:** [`prac-4.pkt`](file:///d:/GIT/CN-practicals/prac-4.pkt) | **Lab Manual:** [`CN-PRACTICAL-4.pdf`](file:///d:/GIT/CN-practicals/PDF/CN-PRACTICAL-4.pdf)
* **Aim:** To implement Variable Length Subnet Masking (VLSM `/27` - Subnet Mask `255.255.255.224`) across 4 subnets connected via 4 routers.

#### 📊 Subnet Allocation Scheme (`255.255.255.224` / Block Size 32)

| Device Group | Assigned Subnet / IP Range | Subnet Mask | Default Gateway |
| :--- | :--- | :--- | :--- |
| **PCs 0, 1, 2** | `192.168.100.2` – `192.168.100.4` | `255.255.255.224` | `192.168.100.1` |
| **PCs 3, 4, 5** | `192.168.100.34` – `192.168.100.36` | `255.255.255.224` | `192.168.100.33` |
| **PCs 6, 7, 8** | `192.168.100.66` – `192.168.100.68` | `255.255.255.224` | `192.168.100.65` |
| **PCs 9, 10, 11** | `192.168.100.98` – `192.168.100.100` | `255.255.255.224` | `192.168.100.97` |

#### 🗺️ Routing Table Next-Hop Configurations

Each router maintains static route entries mapping distant subnet destinations to their specific serial next-hop IP addresses (`192.168.100.129`, `192.168.100.130`, `192.168.100.161`, `192.168.100.162`, `192.168.100.193`, `192.168.100.194`, `192.168.100.225`, `192.168.100.226`).

---

### Practical 5: Integrated Multi-Network Topology Simulation
* **File:** [`prac-5.pkt`](file:///d:/GIT/CN-practicals/prac-5.pkt)
* **Aim:** Comprehensive practical lab combining multi-router topologies, custom IP subnets, LAN switching, and dynamic routing verification.

---

## ⚡ How to Run Simulations

1. Launch **Cisco Packet Tracer**.
2. Open any desired practical file (e.g., `File > Open` -> select [`prac-2.pkt`](file:///d:/GIT/CN-practicals/prac-2.pkt)).
3. Switch between **Realtime** and **Simulation** modes at the bottom-right of Packet Tracer.
4. Use the **Add Simple PDU** tool (`P` shortcut) to test ICMP ping messages between PCs across subnets.
5. Open CLI on routers to inspect running configurations (`show ip route`, `show ip interface brief`, `show ip dhcp binding`).

---

