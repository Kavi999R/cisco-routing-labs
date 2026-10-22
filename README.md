# cisco-routing-labs
Hands-on Cisco networking labs developed in Cisco Packet Tracer, focusing on routing configuration, OSPF, static routes, and network verification.

## Overview

This repository contains hands-on Cisco networking labs developed using Cisco Packet Tracer. The projects focus on configuring and understanding routing between different networks, including a main office and branch network environment.

The labs demonstrate practical networking concepts such as IP addressing, static routing, dynamic routing, and network connectivity between sites.

## Project Scenario

The main project simulates a company network with a **main office and a branch office**.

The objective is to configure the network so that devices at different locations can communicate with each other through properly configured routers and routing protocols.

### Network Environment

* Main Office
* Branch Office
* Cisco routers
* Cisco switches
* End-user devices
* Multiple IP networks
* Inter-site routing

## Skills Demonstrated

* IPv4 addressing and subnetting
* Cisco router configuration
* Static routing
* Dynamic routing
* OSPF
* Network connectivity testing
* Routing table verification
* Cisco IOS CLI
* Basic network design

## Main Office and Branch Network

The topology represents a small business with a main office and a remote branch.

The main office and branch use separate networks and are connected through routers. Routing is configured to allow communication between the different networks.

## Tools Used

* Cisco Packet Tracer
* Cisco IOS CLI

## Project Structure

```text
cisco-routing-labs/
│
├── README.md
│
├── topology/
│   └── network-topology.png
│
├── labs/
| 
|    ├── inter-vlan-routing/
|    ├── acl/
|    ├── ospf/
|    └── branch-network/
│
└── screenshots/
    ├── router-config.png
    ├── routing-table.png
    └── connectivity-test.png
```

## Verification

Network connectivity was verified using Cisco IOS commands such as:

```text
show ip route
show ip interface brief
show running-config
ping

```

These commands were used to verify interface status, routing information, and connectivity between the main office and branch networks.

## IP Addressing Scheme

### Router Interfaces

| Router | Interface | IP Address      | Network    |
| ------ | --------- | --------------- | ---------- |
| R1     | G0/0      | 203.0.113.2/30  | External   |
| R1     | G0/1.10   | 192.168.10.1/24 | Sales      |
| R1     | G0/1.40   | 192.168.40.1/24 | Servers    |
| R1     | G0/1.50   | 192.168.50.1/24 | Wi-Fi      |
| R1     | G0/2      | 10.0.12.1/30    | R1–R2      |
| R2     | G0/0      | 10.0.12.2/30    | R1–R2      |
| R2     | G0/1      | 192.168.20.1/24 | Management |
| R2     | G0/2      | 10.0.23.1/30    | R2–R3      |
| R3     | G0/0      | 192.168.30.1/24 | HR         |
| R3     | G0/1      | 10.0.23.2/30    | R2–R3      |

### VLAN Information

| VLAN ID | VLAN Name  | Network         | Default Gateway |
| ------- | ---------- | --------------- | --------------- |
| 10      | Sales      | 192.168.10.0/24 | 192.168.10.1    |
| 20      | Management | 192.168.20.0/24 | 192.168.20.1    |
| 30      | HR         | 192.168.30.0/24 | 192.168.30.1    |
| 40      | Servers    | 192.168.40.0/24 | 192.168.40.1    |
| 50      | Wi-Fi      | 192.168.50.0/24 | 192.168.50.1    |

### Server Information

| Device          | IP Address    |
| --------------- | ------------- |
| DHCP/DNS Server | 192.168.40.10 |



## What I Learned

Through these labs, I developed practical experience with Cisco IOS, router configuration, IP addressing, routing concepts, and connecting separate networks in a simulated business environment.

This project is part of my ongoing development towards an entry-level networking role.
