# Lab 09: Native VLAN Mismatch & Security

🟡 **Difficulty:** Medium | **Module:** 2 — Switching

## Objective

Identify and fix native VLAN mismatch.

## Topology

**Devices:** 2 Switches (2960) with trunk link + 2 PCs

```
   [PC1]--Fa0/1--[SW1]---trunk---[SW2]--Fa0/1--[PC2]
```

## Requirements

1. Configure trunk between switches
2. On SW1 set native VLAN 99, on SW2 leave default (VLAN 1)
3. Verify — you should see native VLAN mismatch
4. Fix: set native VLAN 99 on both sides
5. Create VLAN 99 on both switches
6. Verify trunk works without errors

## Verification

Submit these outputs after completing the lab:

- `show interfaces trunk (both switches)`
- `show spanning-tree`
- `show cdp neighbors`

## 💡 Hint

> Native VLAN mismatch causes security issues (VLAN hopping attack). Always use a non-default native VLAN.

---

📁 **Structure:**
- `README.md` — Requirements (this file)
- `solution.md` — Solution (don't look before trying!)
- `topology.pkt` — Packet Tracer file (add when you build it)
