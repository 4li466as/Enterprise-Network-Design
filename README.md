<div align="center">
  <h1>🌐 Enterprise Network Design & Implementation</h1>
  <p>A comprehensive Cisco Packet Tracer project featuring a multi-branch enterprise network architecture with advanced routing, switching, and server infrastructure.</p>

  [![Platform: Cisco Packet Tracer](https://img.shields.io/badge/Platform-Cisco_Packet_Tracer-blue.svg)]()
  [![Network: Enterprise](https://img.shields.io/badge/Network-Enterprise_Architecture-green.svg)]()
  [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
</div>

---

## 📖 Table of Contents
- [About the Project](#about-the-project)
- [Architecture Overview](#architecture-overview)
- [Key Technologies & Protocols](#key-technologies--protocols)
- [Services & Servers](#services--servers)
- [Repository Contents](#repository-contents)
- [Getting Started](#getting-started)
- [License](#license)

## 🏢 About the Project

This repository contains the design, implementation, and documentation for a large-scale Enterprise Network. The topology was built using **Cisco Packet Tracer** and spans three major organizational branches connected via an ISP:
1. **CodePort (Main Headquarters)**
2. **TechVista**
3. **NeoCyberia**

Each branch is structured into multiple floors with strict departmental segregation (Management, IT, HR, Finance, Operations, etc.) using VLANs.

## 🗺️ Architecture Overview

The network topology is deeply layered and incorporates the following core design principles:
- **Hierarchical Network Design**: Utilizes Core, Distribution, and Access layer switches.
- **BGP Peer Routing**: The three branches are interconnected over an ISP network using Border Gateway Protocol (BGP).
- **Redundancy & High Availability**: Multiple links between core and distribution switches ensure fault tolerance.
- **Inter-VLAN Routing**: Subnetting is applied meticulously to isolate departmental traffic and broadcast domains.

## ⚙️ Key Technologies & Protocols

- **Routing Protocols**: 
  - `BGP` (Border Gateway Protocol) for ISP WAN routing.
  - `OSPF` / Static Routing for internal branch traffic.
- **Switching**: 
  - `VLANs` (Virtual Local Area Networks) assigned per department.
  - Port Security and MAC address limitations.
- **Dynamic IP Allocation**: 
  - `DHCP` server pools allocated for individual VLANs.
- **Security**: 
  - `AAA` (Authentication, Authorization, and Accounting) via TACACS+/RADIUS servers.
  - `ACLs` (Access Control Lists) to restrict internet and inter-departmental traffic.
  - VTY line encryption and `enable secret` passwords.

## 🖥️ Services & Servers

The headquarters hosts a fully functional datacenter providing services to all end-devices across the VPN/WAN:
- **DNS Server**: Translates internal domains (e.g., `mail.maunexus.com`).
- **HTTP/HTTPS Web Server**: Hosts the company's internal intranet portal.
- **Email Server**: Configured with SMTP/POP3 for intra-organization communication.
- **FTP Server**: Centralized file storage with authentication.
- **Syslog Server**: Centralized logging for network events.
- **NTP Server**: Network Time Protocol for synchronized clocks across routers/switches.
- **Wireless Infrastructure**: WAPs deployed for mobile device access with WPA2-PSK.

## 📁 Repository Contents

- `Enterprise_Network.pkt`: The master Cisco Packet Tracer simulation file containing the fully configured topology.
- `Project_Report.pdf`: A massive, detailed 52-page documentation report outlining the requirements, IP addressing tables, BGP mappings, and configuration commands.

## 🚀 Getting Started

### Prerequisites
- **Cisco Packet Tracer** (Version 8.0 or newer recommended).

### Running the Simulation
1. Clone this repository.
2. Open `Enterprise_Network.pkt` in Cisco Packet Tracer.
3. Wait for the Spanning Tree Protocol (STP) to converge (ports will turn from orange to green).
4. Open the `Project_Report.pdf` to find user credentials and IP tables to test the infrastructure (e.g., pinging across branches, browsing the web server, or sending emails).

## 📝 License

Distributed under the MIT License. See `LICENSE` for more information.
