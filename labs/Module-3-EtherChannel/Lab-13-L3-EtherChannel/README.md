# Lab 13: L3 EtherChannel

🟡 **Difficulty:** Medium | **Module:** 3 — EtherChannel

## Objective

Configure Layer 3 EtherChannel with IP between two L3 switches.

## Topology

**Devices:** 2 L3 Switches (3560) with 2 physical links

```
   [L3-SW1]===Po1(L3)====[L3-SW2]
   10.0.0.1/30            10.0.0.2/30
```

## Requirements

1. On both switches: `no switchport` on Fa0/1-2
2. Create `channel-group 1 mode active` (LACP)
3. On Po1: set IP (10.0.0.1/30 on SW1, 10.0.0.2/30 on SW2)
4. Enable `ip routing`
5. Test ping between switches via EtherChannel

## Verification

Submit these outputs after completing the lab:

- `show etherchannel summary`
- `show ip interface brief`
- `ping between switches`

## 💡 Hint

> L3 EtherChannel: `no switchport` makes the port routed. IP is set on the Po interface, not on physical ports.

---

📁 **Structure:**
- `README.md` — Requirements (this file)
- `solution.md` — Solution (don't look before trying!)
- `topology.pkt` — Packet Tracer file (add when you build it)
