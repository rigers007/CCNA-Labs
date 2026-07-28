# Lab 16: Static Routes

🟡 **Difficulty:** Medium | **Module:** 4 — Routing

## Objective

Configure static routes between 3 routers.

## Topology

**Devices:** 3 Routers (2911) in series + 1 PC per LAN

```
   [PC1]--[R1]---10.0.12.0/30---[R2]---10.0.23.0/30---[R3]--[PC3]
   192.168.1.0/24                 192.168.2.0/24              192.168.3.0/24
```

## Requirements

1. R1 LAN: `192.168.1.0/24`, R2 LAN: `192.168.2.0/24`, R3 LAN: `192.168.3.0/24`
2. WAN R1↔R2: `10.0.12.0/30`, WAN R2↔R3: `10.0.23.0/30`
3. Configure static routes so every LAN can reach every other LAN
4. Do not use default routes — only specific static routes
5. Test end-to-end ping: PC1 → PC3

## Verification

Submit these outputs after completing the lab:

- `show ip route (all 3 routers)`
- `ping PC1→PC3`

## 💡 Hint

> Don't forget: R2 needs static routes to both side LANs, plus it has its own LAN directly connected.

---

📁 **Structure:**
- `README.md` — Requirements (this file)
- `solution.md` — Solution (don't look before trying!)
- `topology.pkt` — Packet Tracer file (add when you build it)
