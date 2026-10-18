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
