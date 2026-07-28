# Lab 32: HSRP + OSPF + NAT/PAT Dual-Edge

🔴 **Difficulty:** Hard | **Module:** 7 — FHRP

## Objective

Dual-edge topology with HSRP, OSPF, and NAT.

## Topology

**Devices:** 2 Routers (edge) + 1 L3 Switch + ISP

```
                    [ISP]
                   /     \
   [R1 edge]-----/       \-----[R2 edge]
       \                         /
        \---[L3-SW]---OSPF----/
            HSRP + SVI
            [PCs]
```

## Requirements

1. OSPF between R1, R2, L3-SW
2. R1, R2: default route + `default-information originate`
3. HSRP on VLAN gateway
4. PAT overload on both routers
5. ACL: permit only HTTP/HTTPS outbound
6. Failover test: shutdown R1 uplink

## Verification

Submit these outputs after completing the lab:

- `show ip ospf neighbor`
- `show standby brief`
- `show ip nat translations`
- `show access-lists`
- `failover test`

## 💡 Hint

> This lab combines everything: OSPF + HSRP + NAT + ACL. This is final exam level.

---

📁 **Structure:**
- `README.md` — Requirements (this file)
- `solution.md` — Solution (don't look before trying!)
- `topology.pkt` — Packet Tracer file (add when you build it)
