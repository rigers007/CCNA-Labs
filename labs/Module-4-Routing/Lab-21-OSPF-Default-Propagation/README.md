# Lab 21: OSPF + Default Route Propagation

🔴 **Difficulty:** Hard | **Module:** 4 — Routing

## Objective

Propagate a default route through OSPF to the internal network.

## Topology

**Devices:** 3 Routers: R1, R2 (edge), R3 + ISP

```
   [R1]---OSPF---[R2]---static---[ISP]
                   |
                 OSPF
                   |
                 [R3]
   R2: default-information originate
```

## Requirements

1. Configure OSPF between R1, R2, R3
2. R2: default route toward ISP (static `0.0.0.0/0`)
3. R2: `default-information originate`
4. Verify: R1 and R3 should have `O*E2` default route
5. Test: PC from R1 LAN should reach ISP loopback
6. Bonus: try `default-information originate always` — what changes?

## Verification

Submit these outputs after completing the lab:

- `show ip route ospf (R1, R3 — look for O*E2)`
- `show ip ospf database (external LSA)`
- `ping end-to-end`

## 💡 Hint

> `always` propagates even when R2 itself doesn't have an active default route. Without `always`, the route must exist.

---

📁 **Structure:**
- `README.md` — Requirements (this file)
- `solution.md` — Solution (don't look before trying!)
- `topology.pkt` — Packet Tracer file (add when you build it)
