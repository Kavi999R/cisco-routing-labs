## Ticket 001: Duplicate IP Address on Management VLAN

**Status:** Resolved - pending final DHCP verification
**Lab:** Inter-VLAN Routing
**Device:** PC2

## Problem

Two PCs on the Management VLAN were configured with the same IP address, resulting in an IP address conflict.

## Symptoms

* PC1 IP address: `192.168.20.13`
* PC2 IP address: `192.168.20.13`
* PC2 default gateway: `0.0.0.0`
* PC2 DNS server: `0.0.0.0`
* Connectivity tests between some devices failed.

## Root Cause

PC1 and PC2 had duplicate IP addresses. PC2 also lacked a valid default gateway and DNS configuration.

## Solution

Changed PC2's IP configuration to DHCP so it could obtain its network settings automatically.

## Verification

The following checks are required:

1. Confirm PC2 receives a unique IP address.
2. Confirm the default gateway is `192.168.20.1`.
3. Confirm the DNS server is `192.168.40.10`.
4. Test connectivity to other network devices.

## Lessons Learned

Duplicate IP addresses can cause unpredictable network communication. DHCP helps prevent address conflicts and automatically supplies the correct network settings.
