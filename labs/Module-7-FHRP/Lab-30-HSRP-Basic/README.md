# Lab 30: Basic HSRP

🔴 **Difficulty:** Hard | **Module:** 7 — FHRP

## Objective

Configure HSRP between two routers for gateway redundancy.

## Topology

**Devices:** 2 Routers + 1 Switch + 2 PCs

```
   [PC1][PC2]---[SW]---[R1: .2, priority 110]
                   \---[R2: .3, priority 100]
   Gateway: 192.168.1.1 (virtual HSRP)
```

## Requirements

1. R1 G0/0: `.2/24`, R2 G0/0: `.3/24`
2. HSRP virtual IP: `192.168.1.1`
3. R1: priority 110 + preempt, R2: priority 100 + preempt
4. PC gateway: `192.168.1.1`
5. R1 = Active (higher priority)
6. Failover test: shutdown R1 G0/0 → R2 becomes Active

## Verification

Submit these outputs after completing the lab:

- `show standby brief`
- `show standby (detail)`
- `continuous ping during failover`

## 💡 Hint

> The virtual IP doesn't belong to any router — it's a shared IP. PCs only know the virtual gateway.

---

📁 **Structure:**
- `README.md` — Requirements (this file)
- `solution.md` — Solution (don't look before trying!)
- `topology.pkt` — Packet Tracer file (add when you build it)
