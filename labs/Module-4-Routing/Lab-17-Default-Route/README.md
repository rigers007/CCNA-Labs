# Lab 17: Default Route & Gateway of Last Resort

🟡 **Difficulty:** Medium | **Module:** 4 — Routing

## Objective

Configure a default route toward the ISP.

## Topology

**Devices:** 2 Routers: R1 (internal) + ISP

```
   [PC1]--[R1]---203.0.113.0/30---[ISP]--Lo0: 8.8.8.8
   192.168.10.0/24
   192.168.20.0/24
```

## Requirements

1. R1 LAN1: `192.168.10.0/24`, LAN2: `192.168.20.0/24`
2. WAN R1↔ISP: `203.0.113.0/30`
3. R1: default route `0.0.0.0/0` toward ISP next-hop
4. ISP: return static routes toward R1's LANs
5. Verify `Gateway of last resort` on R1

## Verification

Submit these outputs after completing the lab:

- `show ip route (R1 — verify * flag)`
- `ping from LAN to ISP loopback`

## 💡 Hint

> Default route (`0.0.0.0/0`) = 'send everything you don't recognize toward the ISP'. Flag `S*` = static default.

---

📁 **Structure:**
- `README.md` — Requirements (this file)
- `solution.md` — Solution (don't look before trying!)
- `topology.pkt` — Packet Tracer file (add when you build it)
