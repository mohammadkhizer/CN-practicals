# 🌐 Computer Networks Laboratory Practicals

Comprehensive collection of Cisco Packet Tracer network simulation files (`.pkt`) and official laboratory manuals (`.pdf`) for the **Computer Networks Laboratory** course.

---

## 📌 Table of Contents

- [Overview](#-overview)
- [Prerequisites & Tools](#-prerequisites--tools)
- [Repository Architecture](#-repository-architecture)
- [Curriculum & Practical Matrix](#-curriculum--practical-matrix)
- [Detailed Practical Breakdown](#-detailed-practical-breakdown)
  - [Practical 1: Introduction to Cisco Packet Tracer](#practical-1-introduction-to-cisco-packet-tracer)
  - [Practical 2: Introduction to Networking Terminal Commands](#practical-2-introduction-to-networking-terminal-commands)
  - [Practical 3: Basic LAN Implementation using Network Switch](#practical-3-basic-lan-implementation-using-network-switch)
  - [Practical 4: Implementation of Various Network Topologies](#practical-4-implementation-of-various-network-topologies)
  - [Practical 5: Inter-Subnet Topology Connecting Two Networks via Switches & Routers](#practical-5-inter-subnet-topology-connecting-two-networks-via-switches--routers)
  - [Practical 6: Multi-Router Static Routing across Class A, B & C Networks](#practical-6-multi-router-static-routing-across-class-a-b--c-networks)
  - [Practical 7: Advanced Subnetting (VLSM /27) & Multi-Router Static Routing Tables](#practical-7-advanced-subnetting-vlsm-27--multi-router-static-routing-tables)
  - [Practical 8: Dynamic Routing Implementation using RIP Protocol (4-Router Mesh)](#practical-8-dynamic-routing-implementation-using-rip-protocol-4-router-mesh)
  - [Practical 9: Virtual LANs (VLANs) Construction, Broadcast Domain Isolation & Traffic Segmentation](#practical-9-virtual-lans-vlans-construction-broadcast-domain-isolation--traffic-segmentation)
  - [Practical 10: Configuration and Analysis of Network Address Translation (NAT)](#practical-10-configuration-and-analysis-of-network-address-translation-nat)
- [Cisco IOS Terminal Command Reference](#-cisco-ios-terminal-command-reference)
- [How to Run Simulations](#-how-to-run-simulations)

---

## ℹ️ Overview

* **Student / Author:** Shaikh Mohammed Khizer  
* **Enrollment Number:** `25CS501D053`  
* **Course:** Computer Networks Laboratory  
* **Simulator:** Cisco Packet Tracer (Compatible with v5.1 / v8.0+)  
* **Key Topics:** LAN Topologies, Switch & Router Configuration, Subnetting & VLSM (`/27`), Static Routing, Dynamic Routing (RIP), VLAN Segmentation (802.1Q access ports), Network Address Translation (Static & Dynamic NAT/PAT), Cisco IOS CLI commands, ICMP PDU verification.

---

## 🛠 Prerequisites & Tools

To inspect the lab manuals and run the interactive network simulations:
1. **Cisco Packet Tracer** (v8.0+ recommended; backward compatible with v5.1).
2. **PDF Reader** (to view original lab manuals stored in the [`PDF/`](file:///d:/Webcraftingexperts/GIT/CN-practicals/PDF) directory).

---

## 📁 Repository Architecture

```
CN-practicals/
├── PDF/                               # Complete Lab Manuals (Practicals 1 to 10)
│   ├── CN-PRACTICAL-1.pdf             # Practical 1: Introduction to Cisco Packet Tracer
│   ├── CN-PRACTICAL-2.pdf             # Practical 2: Networking Terminal Commands
│   ├── CN-PRACTICAL-3.pdf             # Practical 3: Basic LAN using Switch
│   ├── CN-PRACTICAL-4.pdf             # Practical 4: Network Topologies
│   ├── CN-PRACTICAL-5.pdf             # Practical 5: Inter-Subnet Routing via Switches & Routers
│   ├── CN-PRACTICAL-6.pdf             # Practical 6: Static Routing across Class A, B, C
│   ├── CN-PRACTICAL-7.pdf             # Practical 7: VLSM /27 Static Route Tables
│   ├── CN-PRACTICAL-8.pdf             # Practical 8: Dynamic Routing (RIP) across 4 Routers
│   ├── CN-PRACTICAL-9.pdf             # Practical 9: Virtual LANs (VLANs) Segmentation
│   └── CN-PRACTICAL-10.pdf            # Practical 10: Network Address Translation (NAT)
├── Practice-practical/                # Experimental and scratch topologies
│   └── FIrst.pkt                      # Practice Packet Tracer lab file
├── prac-3.pkt                         # Simulation file for Practical 3
├── prac-5.pkt                         # Simulation file for Practical 5
├── prac-6.pkt                         # Simulation file for Practical 6
├── prac-7.pkt                         # Simulation file for Practical 7
├── prac-8.pkt                         # Simulation file for Practical 8
├── prac-9.pkt                         # Simulation file for Practical 9
├── prac-10.pkt                        # Simulation file for Practical 10
├── .gitignore                         # Git exclusion rules (ignores Update/ folder, caches, temporary files)
└── README.md                          # Repository documentation
```

---

## 📊 Curriculum & Practical Matrix

| # | Title / Topic | Simulation File | Lab Manual | Key Concepts / Protocols |
| :-: | :--- | :---: | :---: | :--- |
| **01** | Introduction to Cisco Packet Tracer | — | [`CN-PRACTICAL-1.pdf`](file:///d:/Webcraftingexperts/GIT/CN-practicals/PDF/CN-PRACTICAL-1.pdf) | GUI layout, Realtime vs. Simulation modes, PDU tracing |
| **02** | Networking Terminal Commands | — | [`CN-PRACTICAL-2.pdf`](file:///d:/Webcraftingexperts/GIT/CN-practicals/PDF/CN-PRACTICAL-2.pdf) | 27 IOS & Host commands, Privileged EXEC, Line & Interface config |
| **03** | Basic LAN using Switch | [`prac-3.pkt`](file:///d:/Webcraftingexperts/GIT/CN-practicals/prac-3.pkt) | [`CN-PRACTICAL-3.pdf`](file:///d:/Webcraftingexperts/GIT/CN-practicals/PDF/CN-PRACTICAL-3.pdf) | Cisco 2950-24 switch, copper straight-through, static IP assignment |
| **04** | Implementation of Various Topologies | — | [`CN-PRACTICAL-4.pdf`](file:///d:/Webcraftingexperts/GIT/CN-practicals/PDF/CN-PRACTICAL-4.pdf) | Star, Bus, Ring, Mesh, Hybrid architectures |
| **05** | Inter-Subnet Communication | [`prac-5.pkt`](file:///d:/Webcraftingexperts/GIT/CN-practicals/prac-5.pkt) | [`CN-PRACTICAL-5.pdf`](file:///d:/Webcraftingexperts/GIT/CN-practicals/PDF/CN-PRACTICAL-5.pdf) | Dual routers, serial link (`/30`), multi-subnet routing, default gateways |
| **06** | Multi-Router Static Routing (Class A, B, C) | [`prac-6.pkt`](file:///d:/Webcraftingexperts/GIT/CN-practicals/prac-6.pkt) | [`CN-PRACTICAL-6.pdf`](file:///d:/Webcraftingexperts/GIT/CN-practicals/PDF/CN-PRACTICAL-6.pdf) | 3 Routers, Class A (`10.0.0.0`), Class B (`172.16.0.0`), Class C (`192.168.1.0`) |
| **07** | Advanced Subnetting (VLSM `/27`) | [`prac-7.pkt`](file:///d:/Webcraftingexperts/GIT/CN-practicals/prac-7.pkt) | [`CN-PRACTICAL-7.pdf`](file:///d:/Webcraftingexperts/GIT/CN-practicals/PDF/CN-PRACTICAL-7.pdf) | 4 Routers, block size 32 (`255.255.255.224`), full next-hop static routing |
| **08** | Dynamic Routing via RIP Protocol | [`prac-8.pkt`](file:///d:/Webcraftingexperts/GIT/CN-practicals/prac-8.pkt) | [`CN-PRACTICAL-8.pdf`](file:///d:/Webcraftingexperts/GIT/CN-practicals/PDF/CN-PRACTICAL-8.pdf) | 4 Routers mesh, distance-vector RIP routing, automatic routing table convergence |
| **09** | Virtual LANs (VLANs) & Segmentation | [`prac-9.pkt`](file:///d:/Webcraftingexperts/GIT/CN-practicals/prac-9.pkt) | [`CN-PRACTICAL-9.pdf`](file:///d:/Webcraftingexperts/GIT/CN-practicals/PDF/CN-PRACTICAL-9.pdf) | VLAN 10 & 20, access switchports, broadcast domain isolation |
| **10** | Network Address Translation (NAT) | [`prac-10.pkt`](file:///d:/Webcraftingexperts/GIT/CN-practicals/prac-10.pkt) | [`CN-PRACTICAL-10.pdf`](file:///d:/Webcraftingexperts/GIT/CN-practicals/PDF/CN-PRACTICAL-10.pdf) | Static NAT (Server 1:1), Dynamic NAT with ACL (Private LAN to Public WAN) |

---

## 📘 Detailed Practical Breakdown

---

### Practical 1: Introduction to Cisco Packet Tracer
* **Lab Manual:** [`PDF/CN-PRACTICAL-1.pdf`](file:///d:/Webcraftingexperts/GIT/CN-practicals/PDF/CN-PRACTICAL-1.pdf)
* **Aim:** To study and understand the Cisco Packet Tracer simulation environment, its graphical interface, network components, device configuration methods, and simulation modes for computer network design and analysis.

#### 🖥️ Interface Overview & Core Components
* **Menu Bar & Main Toolbar:** Manage file activities, preferences, canvas zoom, clipboard, and palette tools.
* **Workspace Environments:**
  - **Logical Workspace:** Primary schematic view for placing devices, establishing cabling links, and configuring logical subnets.
  - **Physical Workspace:** Real-world physical layout showing cities, corporate offices, wiring closets, and rack-mounted equipment dimensions.
* **Network Component Box:**
  - **Device Categories:** Routers, Switches, Hubs, Wireless Devices, Connections (Cables), End Devices (PCs, Laptops, Servers, IP Phones), WAN Emulation, Custom Devices, Multi-User.
  - **Cabling Types:** Console, Copper Straight-Through, Copper Cross-Over, Fiber, Phone, Coaxial, Serial DCE, and Serial DTE.
* **Device Configuration Panes:**
  - `Config` tab: User-friendly GUI for setting interface IPs, port status, and routing without raw syntax.
  - `CLI` tab: Direct access to Cisco IOS terminal interface for professional enterprise administration.
  - `Desktop` tab (End Devices): Terminal, Command Prompt, IP Configuration, Web Browser, PC Wireless.
* **Operational Modes:**
  - **Realtime Mode:** Packets propagate continuously, timers advance live, and network protocols (ARP, STP, OSPF, RIP) converge in actual clock time.
  - **Simulation Mode:** Step-by-step packet inspection with play/pause controls, allowing learners to analyze packet headers layer by layer across OSI Layers 1 through 7.

---

### Practical 2: Introduction to Networking Terminal Commands
* **Lab Manual:** [`PDF/CN-PRACTICAL-2.pdf`](file:///d:/Webcraftingexperts/GIT/CN-practicals/PDF/CN-PRACTICAL-2.pdf)
* **Aim:** To understand, execute, and verify the 27 fundamental networking terminal commands across host machines, Layer 2 switches, and routers.

#### 🔀 Cisco IOS Command Modes Hierarchy
1. **User EXEC Mode (`Router>`):** Basic diagnostic read-only commands.
2. **Privileged EXEC Mode (`Router#`):** Entered via `enable`. Allows full verification (`show` commands), debugging, and configuration file operations.
3. **Global Configuration Mode (`Router(config)#`):** Entered via `configure terminal`. Applies parameters that affect the entire device.
4. **Interface Configuration Mode (`Router(config-if)#`):** Configures specific physical or virtual network interfaces (`FastEthernet`, `Serial`, `Vlan`).
5. **Router Configuration Mode (`Router(config-router)#`):** Configures dynamic routing protocols (e.g., `router rip`).
6. **Line Configuration Mode (`Router(config-line)#`):** Configures access lines (`line console 0`, `line vty 0 4`).

#### 📋 Complete 27-Command Taxonomy

```cisco
! 1. Host Verification (PC Command Prompt)
ipconfig                           ! Displays IP, Subnet Mask, Gateway
ipconfig /all                      ! Detailed host network parameters & MAC
ping <destination_ip>              ! Tests end-to-end ICMP reachability
tracert <destination_ip>           ! Hop-by-hop path determination

! 2. Mode Navigation
enable                             ! User EXEC -> Privileged EXEC
configure terminal                 ! Privileged EXEC -> Global Config
interface <type> <number>          ! Enters Interface Config mode
router <protocol>                  ! Enters Routing Protocol Config mode
line <type> <number>               ! Enters Line Config mode
exit                               ! Moves back one level in the hierarchy
end                                ! Returns immediately to Privileged EXEC

! 3. Device Setup & Hardening
hostname <name>                    ! Assigns unique device name
enable secret <password>           ! MD5 encrypted password for privileged mode
password <password>                ! Specifies line access password
login                              ! Enables password authentication on line

! 4. Interface Configuration
ip address <IP> <Subnet-Mask>      ! Sets IPv4 address on interface
no shutdown                        ! Enables the interface (administratively UP)
clock rate 64000                   ! Provides synchronization signal on DCE serial end

! 5. Switch-Only Configuration
interface vlan 1                   ! Accesses switch virtual management interface
ip default-gateway <IP>            ! Configures default gateway for remote switch access

! 6. Static Routing
ip route <net> <mask> <next-hop>   ! Adds manual route to routing table
ip route 0.0.0.0 0.0.0.0 <next-hop>! Configures default gateway of last resort

! 7. Dynamic Routing (RIP)
router rip                         ! Initializes RIP routing process
version 2                          ! Enables RIPv2 (supports VLSM/CIDR)
network <classful-network>         ! Advertises directly connected network
no auto-summary                    ! Disables automatic classful route summarization

! 8. Verification & Persistence
show running-config                ! Displays current configuration in RAM
show ip interface brief            ! Summary table of interfaces, IPs, and link status
show ip route                      ! Displays active IP routing table
copy running-config startup-config ! Commits configuration to NVRAM
```

---

### Practical 3: Basic LAN Implementation using Network Switch
* **Simulation File:** [`prac-3.pkt`](file:///d:/Webcraftingexperts/GIT/CN-practicals/prac-3.pkt)
* **Lab Manual:** [`PDF/CN-PRACTICAL-3.pdf`](file:///d:/Webcraftingexperts/GIT/CN-practicals/PDF/CN-PRACTICAL-3.pdf)
* **Aim:** To implement a Local Area Network (LAN) using a network switch in Cisco Packet Tracer.

#### 📐 Topology & Device Specifications
* **End Devices:** 3 PCs (`PC0`, `PC1`, `PC2`)
* **Switch:** 1 Cisco Catalyst 2950-24 Layer 2 Switch
* **Cabling:** 3 Copper Straight-Through Cables

#### 📊 IP Addressing Table (`192.168.100.0/24`)

| Device | Interface | IP Address | Subnet Mask | Default Gateway |
| :--- | :--- | :--- | :--- | :--- |
| **PC0** | `FastEthernet0` | `192.168.100.2` | `255.255.255.0` | `192.168.100.1` |
| **PC1** | `FastEthernet0` | `192.168.100.3` | `255.255.255.0` | `192.168.100.1` |
| **PC2** | `FastEthernet0` | `192.168.100.4` | `255.255.255.0` | `192.168.100.1` |

#### 🧪 Verification
* Transmit Simple PDU packets from `PC0` to `PC2`.
* Realtime simulation panel confirms **Successful** ICMP delivery across all nodes within the single broadcast domain.

---

### Practical 4: Implementation of Various Network Topologies
* **Lab Manual:** [`PDF/CN-PRACTICAL-4.pdf`](file:///d:/Webcraftingexperts/GIT/CN-practicals/PDF/CN-PRACTICAL-4.pdf)
* **Aim:** To design and implement various standard physical and logical network topologies in Cisco Packet Tracer.

#### 🌐 Architectures Analyzed

1. **Star Topology:**
   - **Structure:** All end stations connect independently to a central intermediate node (Switch/Hub).
   - **Characteristics:** High resilience (individual cable breaks do not impact other hosts), easy expansion, simple fault isolation.
2. **Bus Topology:**
   - **Structure:** Devices share a single linear coaxial backbone cable with terminators on each end.
   - **Characteristics:** Minimal cable required; however, a break in the main backbone halts the entire network.
3. **Ring Topology:**
   - **Structure:** Each device connects directly to two adjacent neighbors, forming a closed continuous circular communication loop.
   - **Characteristics:** Deterministic token-passing data delivery; single-point link failures break loop unless dual-ring topology is deployed.
4. **Mesh Topology:**
   - **Structure:** Dedicated point-to-point links between nodes. Full mesh requires $\frac{n(n-1)}{2}$ links for $n$ nodes.
   - **Characteristics:** Maximum fault tolerance, dedicated channel capacity, zero traffic bottleneck, highest cabling and interface cost.
5. **Hybrid Topology:**
   - **Structure:** Integration of two or more distinct topological architectures (e.g., Star-Bus or Star-Ring).
   - **Characteristics:** Scalable, flexible corporate design accommodating heterogeneous institutional requirements.

---

### Practical 5: Inter-Subnet Topology Connecting Two Networks via Switches & Routers
* **Simulation File:** [`prac-5.pkt`](file:///d:/Webcraftingexperts/GIT/CN-practicals/prac-5.pkt)
* **Lab Manual:** [`PDF/CN-PRACTICAL-5.pdf`](file:///d:/Webcraftingexperts/GIT/CN-practicals/PDF/CN-PRACTICAL-5.pdf)
* **Aim:** To implement a network topology connecting at least two distinct subnets via network switches and routers in Cisco Packet Tracer.

#### 📐 Topology & Device Layout
* **End Devices:** 6 PCs (3 per LAN: `PC0`-`PC2` in LAN 1; `PC3`-`PC5` in LAN 2), 2 Servers (`Server0` in LAN 1, `Server1` in LAN 2).
* **Intermediate Devices:** 2 Cisco 2950-24 Switches, 2 Cisco 1841 Routers with WIC-2T Serial cards.
* **WAN Link:** Router-to-Router connection over Serial link (`10.0.0.0/30`).

#### 📊 Complete IP Addressing Plan

| Device | Interface | IP Address | Subnet Mask | Default Gateway | Role / Network |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Router0** | `FastEthernet0/0` | `192.168.10.1` | `255.255.255.0` | — | LAN 1 Gateway |
| | `Serial0/0/0` | `10.0.0.1` | `255.255.255.252` | — | WAN Link (DCE, Clock 64000) |
| **Router1** | `FastEthernet0/0` | `192.168.200.1` | `255.255.255.0` | — | LAN 2 Gateway |
| | `Serial0/0/0` | `10.0.0.2` | `255.255.255.252` | — | WAN Link (DTE) |
| **PC0** | `FastEthernet0` | `192.168.10.2` | `255.255.255.0` | `192.168.10.1` | LAN 1 Host |
| **PC1** | `FastEthernet0` | `192.168.10.3` | `255.255.255.0` | `192.168.10.1` | LAN 1 Host |
| **PC2** | `FastEthernet0` | `192.168.10.4` | `255.255.255.0` | `192.168.10.1` | LAN 1 Host |
| **Server0** | `FastEthernet0` | `192.168.10.254` | `255.255.255.0` | `192.168.10.1` | LAN 1 Web/DNS Server |
| **PC3** | `FastEthernet0` | `192.168.200.2` | `255.255.255.0` | `192.168.200.1` | LAN 2 Host |
| **PC4** | `FastEthernet0` | `192.168.200.3` | `255.255.255.0` | `192.168.200.1` | LAN 2 Host |
| **PC5** | `FastEthernet0` | `192.168.200.4` | `255.255.255.0` | `192.168.200.1` | LAN 2 Host |
| **Server1** | `FastEthernet0` | `192.168.200.254` | `255.255.255.0` | `192.168.200.1` | LAN 2 Web/DNS Server |

#### ⚙️ Router Configuration & Static Route Insertion

```cisco
! Router0 Configuration
enable
configure terminal
hostname Router0
interface FastEthernet0/0
 ip address 192.168.10.1 255.255.255.0
 no shutdown
exit
interface Serial0/0/0
 ip address 10.0.0.1 255.255.255.252
 clock rate 64000
 no shutdown
exit
ip route 192.168.200.0 255.255.255.0 10.0.0.2
end
write memory
```

```cisco
! Router1 Configuration
enable
configure terminal
hostname Router1
interface FastEthernet0/0
 ip address 192.168.200.1 255.255.255.0
 no shutdown
exit
interface Serial0/0/0
 ip address 10.0.0.2 255.255.255.252
 no shutdown
exit
ip route 192.168.10.0 255.255.255.0 10.0.0.1
end
write memory
```

#### 🧪 Verification
* Transmit Simple PDUs between `PC0` (LAN 1) and `PC3` (LAN 2).
* *Note:* The first attempt may show **Failed** due to ARP table populating and routing table resolution; subsequent attempts result in **Successful** delivery.

---

### Practical 6: Multi-Router Static Routing across Class A, B & C Networks
* **Simulation File:** [`prac-6.pkt`](file:///d:/Webcraftingexperts/GIT/CN-practicals/prac-6.pkt)
* **Lab Manual:** [`PDF/CN-PRACTICAL-6.pdf`](file:///d:/Webcraftingexperts/GIT/CN-practicals/PDF/CN-PRACTICAL-6.pdf)
* **Aim:** To implement a network topology having multiple routers (at least 3 routers with Class A, Class B, and Class C IP addresses) to reach the destination following static routing in Cisco Packet Tracer.

#### 📐 Topology & Device Specifications
* **Routers:** 3 Cisco 1841 Routers with WIC-2T dual-serial interface cards.
* **LAN Subnets Across IP Classes:**
  - **Class A LAN (Router0):** `10.0.0.0/8` (Subnet Mask `255.0.0.0`, Gateway `10.0.0.1` on `Fa0/0`)
  - **Class B LAN (Router1):** `172.16.0.0/16` (Subnet Mask `255.255.0.0`, Gateway `172.16.0.1` on `Fa0/0`)
  - **Class C LAN (Router2):** `192.168.1.0/24` (Subnet Mask `255.255.255.0`, Gateway `192.168.1.1` on `Fa0/0`)
* **Point-to-Point WAN Serial Subnets (`/30` - `255.255.255.252`):**
  - `Router0` ↔ `Router1`: `192.168.10.0/30`
  - `Router0` ↔ `Router2`: `192.168.20.0/30`
  - `Router1` ↔ `Router2`: `192.168.30.0/30`

#### 📊 Router Interface Configuration Matrix

| Router | FastEthernet0/0 (LAN) | Serial0/0/0 (Link) | Serial0/0/1 (Link) |
| :--- | :--- | :--- | :--- |
| **Router0** | `10.0.0.1` / `255.0.0.0` | `192.168.10.1` / `255.255.255.252` (Clock: 64000) | `192.168.20.1` / `255.255.255.252` (Clock: 64000) |
| **Router1** | `172.16.0.1` / `255.255.0.0` | `192.168.10.2` / `255.255.255.252` | `192.168.30.1` / `255.255.255.252` (Clock: 64000) |
| **Router2** | `192.168.1.1` / `255.255.255.0` | `192.168.30.2` / `255.255.255.252` | `192.168.20.2` / `255.255.255.252` |

#### ⚙️ CLI Static Route Setup

```cisco
! Router 0
enable
configure terminal
hostname Router0
interface fastEthernet0/0
 ip address 10.0.0.1 255.0.0.0
 no shutdown
exit
interface serial0/0/0
 ip address 192.168.10.1 255.255.255.252
 clock rate 64000
 no shutdown
exit
interface serial0/0/1
 ip address 192.168.20.1 255.255.255.252
 clock rate 64000
 no shutdown
exit
ip route 172.16.0.0 255.255.0.0 192.168.10.2
ip route 192.168.1.0 255.255.255.0 192.168.20.2
end
write memory
```

```cisco
! Router 1
enable
configure terminal
hostname Router1
interface fastEthernet0/0
 ip address 172.16.0.1 255.255.0.0
 no shutdown
exit
interface serial0/0/0
 ip address 192.168.10.2 255.255.255.252
 no shutdown
exit
interface serial0/0/1
 ip address 192.168.30.1 255.255.255.252
 clock rate 64000
 no shutdown
exit
ip route 10.0.0.0 255.0.0.0 192.168.10.1
ip route 192.168.1.0 255.255.255.0 192.168.30.2
end
write memory
```

```cisco
! Router 2
enable
configure terminal
hostname Router2
interface fastEthernet0/0
 ip address 192.168.1.1 255.255.255.0
 no shutdown
exit
interface serial0/0/0
 ip address 192.168.30.2 255.255.255.252
 no shutdown
exit
interface serial0/0/1
 ip address 192.168.20.2 255.255.255.252
 no shutdown
exit
ip route 10.0.0.0 255.0.0.0 192.168.20.1
ip route 172.16.0.0 255.255.0.0 192.168.30.1
end
write memory
```

---

### Practical 7: Advanced Subnetting (VLSM /27) & Multi-Router Static Routing Tables
* **Simulation File:** [`prac-7.pkt`](file:///d:/Webcraftingexperts/GIT/CN-practicals/prac-7.pkt)
* **Lab Manual:** [`PDF/CN-PRACTICAL-7.pdf`](file:///d:/Webcraftingexperts/GIT/CN-practicals/PDF/CN-PRACTICAL-7.pdf)
* **Aim:** To implement static IP routing to configure a multi-router network utilizing Variable Length Subnet Masking (VLSM `/27` - `255.255.255.224`).

#### 📊 Subnet Allocation Scheme (`/27` | Block Size: 32)
* **Common Subnet Mask:** `255.255.255.224`

| LAN / Group | Subnet Address | Usable Host Range | Default Gateway | Connected Devices |
| :--- | :--- | :--- | :--- | :--- |
| **LAN 0** | `192.168.100.0/27` | `192.168.100.2` – `.30` | `192.168.100.1` | `PC0`, `PC1`, `PC2` |
| **LAN 1** | `192.168.100.32/27` | `192.168.100.34` – `.62` | `192.168.100.33` | `PC3`, `PC4`, `PC5` |
| **LAN 2** | `192.168.100.64/27` | `192.168.100.66` – `.94` | `192.168.100.65` | `PC6`, `PC7`, `PC8` |
| **LAN 3** | `192.168.100.96/27` | `192.168.100.98` – `.126` | `192.168.100.97` | `PC9`, `PC10`, `PC11` |

#### 🗺️ Router Interface Addressing

| Router | FastEthernet0/0 | Serial0/0/0 | Serial0/0/1 |
| :--- | :--- | :--- | :--- |
| **Router0** | `192.168.100.1` | `192.168.100.129` (Clock 64000) | `192.168.100.226` (Clock 64000) |
| **Router1** | `192.168.100.33` | `192.168.100.130` (Clock 64000) | `192.168.100.161` (Clock 64000) |
| **Router2** | `192.168.100.65` | `192.168.100.193` (Clock 64000) | `192.168.100.162` (Clock 64000) |
| **Router3** | `192.168.100.97` | `192.168.100.194` (Clock 64000) | `192.168.100.225` (Clock 64000) |

#### 🧭 Complete Static Routing Tables

```cisco
! Router 0 Static Routes
ip route 192.168.100.32  255.255.255.224 192.168.100.130
ip route 192.168.100.64  255.255.255.224 192.168.100.130
ip route 192.168.100.96  255.255.255.224 192.168.100.225
ip route 192.168.100.160 255.255.255.224 192.168.100.130
ip route 192.168.100.192 255.255.255.224 192.168.100.225

! Router 1 Static Routes
ip route 192.168.100.0   255.255.255.224 192.168.100.129
ip route 192.168.100.64  255.255.255.224 192.168.100.162
ip route 192.168.100.96  255.255.255.224 192.168.100.162
ip route 192.168.100.192 255.255.255.224 192.168.100.162
ip route 192.168.100.224 255.255.255.224 192.168.100.129

! Router 2 Static Routes
ip route 192.168.100.0   255.255.255.224 192.168.100.161
ip route 192.168.100.32  255.255.255.224 192.168.100.161
ip route 192.168.100.96  255.255.255.224 192.168.100.194
ip route 192.168.100.128 255.255.255.224 192.168.100.161
ip route 192.168.100.224 255.255.255.224 192.168.100.194

! Router 3 Static Routes
ip route 192.168.100.0   255.255.255.224 192.168.100.226
ip route 192.168.100.32  255.255.255.224 192.168.100.226
ip route 192.168.100.64  255.255.255.224 192.168.100.193
ip route 192.168.100.128 255.255.255.224 192.168.100.226
ip route 192.168.100.160 255.255.255.224 192.168.100.193
```

---

### Practical 8: Dynamic Routing Implementation using RIP Protocol (4-Router Mesh)
* **Simulation File:** [`prac-8.pkt`](file:///d:/Webcraftingexperts/GIT/CN-practicals/prac-8.pkt)
* **Lab Manual:** [`PDF/CN-PRACTICAL-8.pdf`](file:///d:/Webcraftingexperts/GIT/CN-practicals/PDF/CN-PRACTICAL-8.pdf)
* **Aim:** To implement the RIP dynamic routing protocol in the given network having at least 4 routers.

#### 📐 Topology & Addressing Scheme
* **LAN Subnets:**
  - **LAN 0 (Router0):** `192.168.40.0/24` (PCs 0 & 1: `.2`, `.3`; Gateway: `192.168.40.1`)
  - **LAN 1 (Router1):** `192.168.10.0/24` (PCs 2 & 3: `.2`, `.3`; Gateway: `192.168.10.1`)
  - **LAN 2 (Router2):** `192.168.20.0/24` (PCs 4 & 5: `.2`, `.3`; Gateway: `192.168.20.1`)
  - **LAN 3 (Router3):** `192.168.30.0/24` (PCs 6 & 7: `.2`, `.3`; Gateway: `192.168.30.1`)
* **Serial Mesh Subnets:**
  - `Router0` ↔ `Router1`: `192.168.50.0/24` (`Router0` Se0/0/0: `.3`, `Router1` Se0/0/0: `.2`)
  - `Router0` ↔ `Router3`: `192.168.60.0/24` (`Router0` Se0/0/1: `.2`, `Router3` Se0/0/1: `.3`)
  - `Router2` ↔ `Router3`: `192.168.70.0/24` (`Router2` Se0/0/0: `.3`, `Router3` Se0/0/0: `.2`)
  - `Router1` ↔ `Router2`: `192.168.80.0/24` (`Router1` Se0/0/1: `.2`, `Router2` Se0/0/1: `.3`)

#### ⚙️ RIP Routing Protocol Declarations

```cisco
! Router 0 RIP Config
router rip
 network 192.168.40.0
 network 192.168.50.0
 network 192.168.60.0
exit

! Router 1 RIP Config
router rip
 network 192.168.10.0
 network 192.168.50.0
 network 192.168.80.0
exit

! Router 2 RIP Config
router rip
 network 192.168.20.0
 network 192.168.70.0
 network 192.168.80.0
exit

! Router 3 RIP Config
router rip
 network 192.168.30.0
 network 192.168.60.0
 network 192.168.70.0
exit
```

#### 🧪 Verification & Protocol Convergence
* Routing Information Protocol uses hop-count metric (maximum 15 hops) and periodic timer updates.
* Routing tables dynamically populate neighbor networks.
* Cross-network ICMP packet delivery reaches **Successful** status across all 4 quadrants of the topology.

---

### Practical 9: Virtual LANs (VLANs) Construction, Broadcast Domain Isolation & Traffic Segmentation
* **Simulation File:** [`prac-9.pkt`](file:///d:/Webcraftingexperts/GIT/CN-practicals/prac-9.pkt)
* **Lab Manual:** [`PDF/CN-PRACTICAL-9.pdf`](file:///d:/Webcraftingexperts/GIT/CN-practicals/PDF/CN-PRACTICAL-9.pdf)
* **Aim:** Explore the utility of Virtual LANs (VLANs) by constructing a network infrastructure configured with multiple distinct VLANs to manage broadcast domains and segment traffic.

#### 📐 Topology & Port Assignments
* **End Devices:** 4 PCs connected to a single Cisco 2950-24 Switch on subnet `192.168.10.0/24`.
* **VLAN Segmentation:**
  - **VLAN 10:** Assigned to ports `FastEthernet0/1` (`PC0`: `192.168.10.2`) and `FastEthernet0/3` (`PC2`: `192.168.10.4`).
  - **VLAN 20:** Assigned to ports `FastEthernet0/2` (`PC1`: `192.168.10.3`) and `FastEthernet0/4` (`PC3`: `192.168.10.5`).

#### ⚙️ Switch Port & VLAN CLI Configuration

```cisco
enable
configure terminal
hostname Switch0

! 1. Define VLAN 10 and assign access ports
vlan 10
 name Department_A
exit
interface fastEthernet 0/1
 switchport mode access
 switchport access vlan 10
exit
interface fastEthernet 0/3
 switchport mode access
 switchport access vlan 10
exit

! 2. Define VLAN 20 and assign access ports
vlan 20
 name Department_B
exit
interface fastEthernet 0/2
 switchport mode access
 switchport access vlan 20
exit
interface fastEthernet 0/4
 switchport mode access
 switchport access vlan 20
exit
end
write memory
```

#### 🧪 Verification & Broadcast Domain Analysis
* **Intra-VLAN Communication (`PC0` ↔ `PC2` on VLAN 10):** PDU transmission is **Successful**.
* **Intra-VLAN Communication (`PC1` ↔ `PC3` on VLAN 20):** PDU transmission is **Successful**.
* **Inter-VLAN Communication (`PC0` [VLAN 10] ↔ `PC1` [VLAN 20]):** PDU transmission **Fails**.
* **Conclusion:** Even though all hosts reside on the same IP subnet (`192.168.10.0/24`), Layer 2 frame forwarding is restricted strictly to members of the same VLAN ID. This demonstrates broadcast domain containment and traffic security without physical infrastructure separation.

---

### Practical 10: Configuration and Analysis of Network Address Translation (NAT)
* **Simulation File:** [`prac-10.pkt`](file:///d:/Webcraftingexperts/GIT/CN-practicals/prac-10.pkt)
* **Lab Manual:** [`PDF/CN-PRACTICAL-10.pdf`](file:///d:/Webcraftingexperts/GIT/CN-practicals/PDF/CN-PRACTICAL-10.pdf)
* **Aim:** Configure and analyze Network Address Translation (NAT) protocol in Cisco Packet Tracer to translate private IP addresses to public IP addresses.

#### 📐 Topology & Network Layout
* **Inside Private LAN (Router0 side):** Hosts (`PC0`: `192.168.10.2/24`, Gateway: `192.168.10.1`) connected via Switch to `Router0` (`Fa0/0`: `192.168.10.1`).
* **Public WAN Serial Backbone:** `Router0` (`Serial0/0/0`: `200.200.200.2/24`) connected to `Router1` (`Serial0/0/0`: `200.200.200.3/24`, Clock rate: `64000`).
* **Outside Server LAN (Router1 side):** `Router1` (`Fa0/0`: `172.16.0.1/16`) connected to Web Server (`Server0`: `172.16.255.254/16`, Gateway: `172.16.0.1`).

#### ⚙️ CLI NAT Configurations

##### 1. Static NAT on Router 1 (Public Server Translation)
Maps the internal server IP `172.16.255.254` statically to public IP `200.200.200.3`:

```cisco
enable
configure terminal
hostname Router1
interface fastEthernet0/0
 ip address 172.16.0.1 255.255.0.0
 no shutdown
 ip nat inside
exit
interface serial 0/0/0
 ip address 200.200.200.3 255.255.255.0
 clock rate 64000
 no shutdown
 ip nat outside
exit
ip route 0.0.0.0 0.0.0.0 serial 0/0/0

! Static NAT entry: 1-to-1 Private Server to Public IP
ip nat inside source static 172.16.255.254 200.200.200.3
end
write memory
```

##### 2. Dynamic NAT / Overload on Router 0 (Inside LAN Translation)
Translates the entire private subnet `192.168.10.0/24` dynamically through the serial WAN interface using an Access Control List (ACL):

```cisco
enable
configure terminal
hostname Router0
interface fastEthernet0/0
 ip address 192.168.10.1 255.255.255.0
 no shutdown
 ip nat inside
exit
interface serial0/0/0
 ip address 200.200.200.2 255.255.255.0
 no shutdown
 ip nat outside
exit
ip route 0.0.0.0 0.0.0.0 serial 0/0/0

! ACL 1: Identify inside private traffic eligible for NAT
access-list 1 permit 192.168.10.0 0.0.0.255

! Dynamic NAT Overload via Outgoing Serial Interface
ip nat inside source list 1 interface serial 0/0/0
end
write memory
```

#### 🧪 Verification & Web Browser Test
1. On `PC0` (`192.168.10.2`), click `Desktop` > `Web Browser`.
2. Enter the public address `http://200.200.200.3` in the URL bar and click **Go**.
3. The server's HTTP default web page loads successfully.
4. On `Router0` and `Router1`, run `show ip nat translations` in Privileged EXEC mode to inspect active NAT translation tables and port mappings.

---

## 📖 Cisco IOS Terminal Command Reference

A quick reference guide for essential commands across Cisco switches and routers:

| Category | Command Syntax | Description |
| :--- | :--- | :--- |
| **Host Diagnostic** | `ipconfig /all` | Displays full TCP/IP configuration, DHCP, and physical MAC address |
| | `ping <IP>` | Sends ICMP echo requests to test destination reachability |
| | `tracert <IP>` | Traces the router hops packets traverse to reach target |
| **Mode Switching** | `enable` | Enters Privileged EXEC mode (`#`) |
| | `configure terminal` | Enters Global Configuration mode (`(config)#`) |
| | `interface <type> <port>` | Enters Interface Configuration mode (`(config-if)#`) |
| | `exit` / `end` | Step back one mode level / Return straight to Privileged EXEC |
| **Interface Setup** | `ip address <IP> <mask>` | Sets IP address and subnet mask on an interface |
| | `no shutdown` | Administratively turns the interface power ON |
| | `clock rate 64000` | Sets hardware timing synchronization on DCE serial interfaces |
| **Switch VLAN** | `vlan <ID>` | Creates or configures a Virtual LAN |
| | `switchport mode access` | Sets interface into non-trunking access mode |
| | `switchport access vlan <ID>` | Binds interface to the specified VLAN |
| **Routing** | `ip route <net> <mask> <hop>` | Installs static route via specified next-hop gateway |
| | `router rip` | Starts RIP routing daemon |
| | `network <net>` | Publishes connected classful network in RIP updates |
| **NAT** | `ip nat inside / outside` | Designates interface as boundary inside or outside |
| | `ip nat inside source static` | 1-to-1 static private-to-public mapping |
| | `ip nat inside source list` | Many-to-one dynamic translation bound to ACL |
| **Inspection & Save** | `show ip interface brief` | One-line summary table of interface status, IP, and protocol state |
| | `show ip route` | Prints active IP routing table |
| | `show ip nat translations` | Displays current active NAT translation bindings |
| | `copy run start` | Saves active running configuration to persistent NVRAM |

---

## ⚡ How to Run Simulations

1. Launch **Cisco Packet Tracer** (v8.0+ or v5.1+).
2. Open any desired practical simulation file (e.g., `File` > `Open` -> select [`prac-6.pkt`](file:///d:/Webcraftingexperts/GIT/CN-practicals/prac-6.pkt)).
3. Toggle between **Realtime** and **Simulation** modes located in the bottom-right status bar.
4. Use the **Add Simple PDU** tool (`P` shortcut) to send ICMP ping packets between end devices across subnets.
5. Double-click any router or switch to open the **CLI tab** and run verification commands (`show ip route`, `show ip interface brief`, `show ip nat translations`).
6. Consult the corresponding manual in the [`PDF/`](file:///d:/Webcraftingexperts/GIT/CN-practicals/PDF) directory for step-by-step guidance and theoretical background.

---
