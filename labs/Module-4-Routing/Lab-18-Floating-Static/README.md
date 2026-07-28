# Lab 18: Floating Static Route

🟡 **Difficulty:** Medium | **Module:** 4 — Routing

## Objective

Configure a backup link with a floating static route (higher AD).

## Topology

**Devices:** 2 Routers with 2 links: primary + backup

```
   [R1]===primary (G0/0): 10.0.0.0/30===[R2]
   [R1]---backup  (S0/0): 10.0.1.0/30---[R2]
   LAN1                                  LAN2
```

## Requirements

1. Primary: `10.0.0.0/30` (G0/0↔G0/0), Backup: `10.0.1.0/30` (S0/0↔S0/0)
2. Static route toward other LAN via primary next-hop
3. Floating static route with AD=10 via backup
4. Verify: only primary route should appear
5. Shutdown primary → floating route activates automatically
6. No shutdown primary → original route returns

## Verification

Submit these outputs after completing the lab:

- `show ip route (3 phases: normal, failover, recovery)`
- `ping during failover`

## 💡 Hint

> Default AD for static route = 1. Floating route with AD=10 only installs when the primary disappears.

---

📁 **Structure:**
- `README.md` — Requirements (this file)
- `solution.md` — Solution (don't look before trying!)
- `topology.pkt` — Packet Tracer file (add when you build it)
