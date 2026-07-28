# Lab 28: Port Security

🟡 **Difficulty:** Medium | **Module:** 6 — Security

## Objective

Configure port security to restrict MAC addresses.

## Topology

**Devices:** 1 Switch (2960) + 2 PCs

```
   [PC1]--Fa0/1--[SW1]
   [PC2] (for violation test)
```

## Requirements

1. Fa0/1: `switchport port-security`, maximum 1, violation shutdown
2. `switchport port-security mac-address sticky`
3. Connect PC1 → learn MAC (sticky)
4. Disconnect PC1, connect PC2 → err-disabled
5. `errdisable recovery cause psecure-violation`, interval 30

## Verification

Submit these outputs after completing the lab:

- `show port-security interface Fa0/1`
- `show port-security address`
- `show interfaces status err-disabled`

## 💡 Hint

> Sticky MAC is learned automatically and saved to running-config. `copy run start` makes it permanent.

---

📁 **Structure:**
- `README.md` — Requirements (this file)
- `solution.md` — Solution (don't look before trying!)
- `topology.pkt` — Packet Tracer file (add when you build it)
