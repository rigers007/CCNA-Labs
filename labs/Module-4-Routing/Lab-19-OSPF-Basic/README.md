# Lab 19: OSPF Single-Area Basics

🟡 **Difficulty:** Medium | **Module:** 4 — Routing

## Objective

Configure OSPF single-area between 3 routers.

## Topology

**Devices:** 3 Routers in a triangle + 1 LAN each

```
           [R1]--LAN: 10.1.1.0/24
          /     \
   10.0.12.0    10.0.13.0
        /           \
     [R2]---10.0.23.0---[R3]
   10.2.2.0/24        10.3.3.0/24
```

## Requirements

1. LANs: R1=`10.1.1.0/24`, R2=`10.2.2.0/24`, R3=`10.3.3.0/24`
2. WANs: `10.0.12.0/30`, `10.0.23.0/30`, `10.0.13.0/30`
3. OSPF process 1, area 0 on all 3 routers
4. Network statements with correct wildcard masks
5. Set router-id manually: `1.1.1.1`, `2.2.2.2`, `3.3.3.3`
6. `passive-interface` on LAN interfaces

## Verification

Submit these outputs after completing the lab:

- `show ip ospf neighbor`
- `show ip ospf interface brief`
- `show ip route ospf`
- `ping end-to-end`

## 💡 Hint

> Wildcard mask = inverse of subnet mask. /24 → 0.0.0.255, /30 → 0.0.0.3. passive-interface stops OSPF hellos on LAN.

---

📁 **Structure:**
- `README.md` — Requirements (this file)
- `solution.md` — Solution (don't look before trying!)
- `topology.pkt` — Packet Tracer file (add when you build it)
