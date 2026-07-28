# Lab 20: OSPF Cost Manipulation & DR/BDR

🔴 **Difficulty:** Hard | **Module:** 4 — Routing

## Objective

Manipulate OSPF cost and verify DR/BDR election.

## Topology

**Devices:** 3 Routers + 1 multi-access segment

```
   [R1]---[R2]---[R3]
     \      |      /
      \     |     /
    [Multi-access segment]
```

## Requirements

1. Configure OSPF as in Lab 19
2. Identify which router was elected DR and BDR in the multi-access segment
3. Change OSPF priority: R1=100 (DR), R2=50 (BDR), R3=0 (never DR)
4. Run `clear ip ospf process` for re-election
5. Change OSPF cost on R1↔R3 link (`ip ospf cost 100`) — verify routing table change
6. Configure `auto-cost reference-bandwidth 10000`

## Verification

Submit these outputs after completing the lab:

- `show ip ospf neighbor (DR/BDR roles)`
- `show ip ospf interface (cost values)`
- `show ip route ospf`

## 💡 Hint

> Priority 0 = never DR/BDR. DR election only happens once — requires clear process to re-elect.

---

📁 **Structure:**
- `README.md` — Requirements (this file)
- `solution.md` — Solution (don't look before trying!)
- `topology.pkt` — Packet Tracer file (add when you build it)
