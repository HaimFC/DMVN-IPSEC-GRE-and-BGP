# DMVPN Lab Project

## Overview

This project presents a comprehensive lab environment to study and implement a **Dynamic Multipoint Virtual Private Network (DMVPN)** using **GNS3**. It includes configurations for GRE, IPsec, EIGRP, NAT, and other networking protocols in a hub-and-spoke topology. The lab provides practical exercises for configuring, testing, and securing VPN connections in enterprise environments.

The lab is structured into preparation, installation, configuration, and verification steps, complete with theoretical questions and discussion topics.

---

## Features

- **DMVPN Configuration**:
  - Full-mesh DMVPN (Phase 1).
  - Scalable hub-and-spoke DMVPN (Phases 2 & 3).
- **Routing Protocols**:
  - BGP for external routes.
  - EIGRP and OSPF for internal routing.
- **Encryption**:
  - Secure VPN communication with IPsec.
- **Network Address Translation (NAT)**:
  - Configure NAT to enable internet access simulation.
- **Wireshark Analysis**:
  - Packet capture for protocol verification and debugging.
- **Hands-on Exercises**:
  - Preparatory questions, step-by-step instructions, and validation tasks with screenshots.

---

## Prerequisites

1. **Operating System**:
   - Windows 10 or Windows 11.

2. **Virtualization Support**:
   - Intel CPU with virtualization technology enabled.
   - Check your CPU compatibility [here](https://www.intel.com/content/www/us/en/support/articles/000005486/processors.html).

3. **Software Requirements**:
   - [GNS3](https://gns3.com/software/download-vm) (matching GNS3 VM version).
   - [VMware Workstation Player](https://www.vmware.com/products/workstation-player/workstation-player-evaluation.html) or VMware Workstation Pro.
   - Pre-configured Cisco router and switch images:
     - [Router Image](https://upw.io/4zu/vios-adventerprisek9-m.vmdk.SPA.156-2.T.qcow2)
     - [Switch Image](https://upw.io/75f/vios_l2-adventerprisek9-m.SSA.high_iron_20180619.qcow2)

---

## Topology Description

The lab simulates a real-world enterprise network with:
- **Hub-and-Spoke Design**: A central hub router and multiple spoke sites.
- **Protocols**:
  - **BGP**: External routing.
  - **OSPF & EIGRP**: Internal routing.
  - **mGRE**: Simplified tunnel configuration.
  - **NHRP**: Resolves next-hop details dynamically.
  - **IPsec**: Ensures secure communication.

### Network Topology
The lab environment is designed with:
- **Hub Router (Customer 1)**: Central hub for the DMVPN.
- **Spoke Routers (Customer 2, 3, 4)**: Connected to the hub.
- **ISP Backbone**: Enables routing across the network.
- **Ubuntu PCs**: Docker containers emulating client devices.

---

## Lab Steps

1. **Preparation**:
   - Install GNS3 and GNS3 VM.
   - Configure virtualization support and import necessary Cisco appliance images.
   - Set up routers, switches, and Docker containers in GNS3.

2. **Configuration**:
   - **Routing Protocols**:
     - Configure BGP for ISP backbone routing.
     - Use OSPF for dynamic routing within the ISP.
   - **DMVPN**:
     - Establish mGRE tunnels with NHRP.
     - Implement hub-and-spoke topology.
   - **NAT**:
     - Enable NAT on customer routers for internet access.
   - **IPsec**:
     - Secure DMVPN tunnels with IPsec encryption.

3. **Verification**:
   - Use Wireshark to capture and analyze traffic.
   - Validate routing and DMVPN tunnel status using commands like:
     - `show ip bgp`
     - `show ip eigrp neighbors`
     - `show dmvpn`
   - Test connectivity with ping and traceroute commands.

---

## Theoretical Questions

1. **GRE Protocol**:
   - How does GRE differ from other tunneling protocols (e.g., L2TP, IPIP)?
2. **IPsec Basics**:
   - Explain the role of IPsec in securing VPNs.
3. **DMVPN Components**:
   - Key components and their roles.
4. **DMVPN Phases**:
   - Characteristics of each phase.
5. **Routing Protocols**:
   - Integration of EIGRP, OSPF, or BGP with DMVPN.
6. **NHRP**:
   - Its significance in DMVPN.
7. **mGRE**:
   - Benefits over traditional GRE.

---

## How to Use

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/dmvpn-lab.git
