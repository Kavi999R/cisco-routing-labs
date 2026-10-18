# Branch Network

## Overview

This project simulates a business network connecting a main office and remote departments using Cisco Packet Tracer.

The network uses three routers (R1, R2 and R3) to provide communication between different departments and network locations.

## Network Features

* Three-router network design
* Multiple VLANs
* Sales, Management, HR, Servers and Wi-Fi networks
* Multi-area OSPF
* DHCP configuration
* Network Address Translation (NAT)
* Access Control Lists (ACLs)
* Inter-network connectivity

## OSPF Area Design

| Area   | Network                        |
| ------ | ------------------------------ |
| Area 0 | Backbone links between routers |
| Area 1 | Sales, Servers and Wi-Fi       |
| Area 2 | Management                     |
| Area 3 | HR                             |

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

## Verification Commands

```cisco
show ip ospf neighbor
show ip route
show ip interface brief
show access-lists
show vlan brief
ping
traceroute
```

## Learning Outcomes

This project helped me develop practical experience in designing a multi-router network, configuring multi-area OSPF, implementing network services and applying basic network security controls.
