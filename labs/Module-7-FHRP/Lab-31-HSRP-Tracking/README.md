# Lab 31: HSRP with Tracking

🔴 **Difficulty:** Hard | **Module:** 7 — FHRP

## Objective

HSRP tracking — uplink goes down, priority decreases automatically.

## Topology

**Devices:** 2 Routers + 1 Switch + ISP

```
   [PCs]---[SW]---[R1]---uplink G0/1---[ISP]
                \-[R2]---uplink G0/1---[ISP]
   HSRP: R1 active, track G0/1
```

## Requirements

1. HSRP as in Lab 30
2. R1: `standby 1 track G0/1 decrement 20`
3. With G0/1 up: R1 Active (110)
4. Shutdown G0/1 → priority drops to 90 → R2 becomes Active
5. No shutdown G0/1 → R1 recovers (preempt)

## Verification

Submit these outputs after completing the lab:

- `show standby brief (before/after shutdown)`
- `show standby (tracked interface)`

## 💡 Hint

> Track decrement must be calculated: if R1=110, R2=100, decrement must be > 10 for failover to occur.

---

📁 **Structure:**
- `README.md` — Requirements (this file)
- `solution.md` — Solution (don't look before trying!)
- `topology.pkt` — Packet Tracer file (add when you build it)
