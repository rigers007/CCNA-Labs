# Lab 10: Rapid PVST+ and PortFast

🟡 **Difficulty:** Medium | **Module:** 2 — Switching

## Objective

Configure Rapid PVST+ and optimize convergence with PortFast/BPDU Guard.

## Topology

**Devices:** 2 Switches (2960) + 2 PCs

```
   [PC1]--Fa0/1--[SW1]---trunk---[SW2]--Fa0/1--[PC2]
```

## Requirements

1. Change STP mode to rapid-pvst (`spanning-tree mode rapid-pvst`)
2. On access ports (PCs): enable PortFast
3. On access ports: enable BPDU Guard
4. Verify PCs go directly to forwarding (no 30s delay)
5. Test: connect another switch to a BPDU Guard port → should err-disable

## Verification

Submit these outputs after completing the lab:

- `show spanning-tree summary`
- `show spanning-tree interface Fa0/1 detail`
- `show interfaces status err-disabled`

## 💡 Hint

> PortFast skips directly to forwarding (no 30s STP delay). BPDU Guard protects against unauthorized switches.

---

📁 **Structure:**
- `README.md` — Requirements (this file)
- `solution.md` — Solution (don't look before trying!)
- `topology.pkt` — Packet Tracer file (add when you build it)
