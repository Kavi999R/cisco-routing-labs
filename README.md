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
traceroute
```

These commands were used to verify interface status, routing information, and connectivity between the main office and branch networks.

## What I Learned

Through these labs, I developed practical experience with Cisco IOS, router configuration, IP addressing, routing concepts, and connecting separate networks in a simulated business environment.

This project is part of my ongoing development towards an entry-level networking role.
