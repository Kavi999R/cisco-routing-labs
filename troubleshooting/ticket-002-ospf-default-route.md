## Ticket 002: Default Route Not Advertised Through OSPF

**Status:** Resolved
**Lab:** Branch Network
**Device:** R1, R2, R3

## Problem

Branch routers R2 and R3 could not reach the external server because they did not have a default route to external networks.

## Symptoms

* R1 had a static default route pointing to the ISP.
* R2 and R3 did not initially learn a default route through OSPF.
* External connectivity from the branch routers was unsuccessful.

## Root Cause

R1 had a static default route but was not advertising it to other OSPF routers.

## Solution

Configured R1 to advertise its default route through OSPF:

```cisco
enable
configure terminal
router ospf 1
default-information originate
end
```

R1 already had the static default route:

```cisco
ip route 0.0.0.0 0.0.0.0 203.0.113.1
```

## Verification

Checked the routing tables on R2 and R3:

```cisco
show ip route
```

Both routers learned the default route through OSPF, displayed as:

```text
O*E2 0.0.0.0/0
```

Also verified OSPF neighbor relationships and external connectivity.

## Lessons Learned

A static default route on one router is not automatically advertised to other OSPF routers. The `default-information originate` command allows R1 to advertise the default route through OSPF when a default route exists in its routing table.
