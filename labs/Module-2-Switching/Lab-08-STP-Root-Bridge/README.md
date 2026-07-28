# Lab 08: STP Verification & Root Bridge

🟡 **Difficulty:** Medium | **Module:** 2 — Switching

## Objective

Verify STP, identify root bridge, and manipulate priority.

## Topology

**Devices:** 3 Switches (2960) connected in a triangle

```
         [SW1]
        /     \
   Fa0/1     Fa0/2
      /         \
   [SW2]---Fa0/1---[SW3]
```

## Requirements

1. Connect switches: SW1↔SW2, SW2↔SW3, SW1↔SW3
2. Without changing anything, verify which switch is the root bridge
3. Identify which ports are Root, Designated, and Blocked
4. Change SW1 priority to 4096 to force it as root bridge
5. Verify again — SW1 should now be root

## Verification

Submit these outputs after completing the lab:

- `show spanning-tree (all 3 switches, before and after)`
- `Diagram of RP/DP/BP ports`

## 💡 Hint

> Root bridge is elected by lowest MAC address (if priority is equal). With priority 4096, SW1 always wins.

---

📁 **Structure:**
- `README.md` — Requirements (this file)
- `solution.md` — Solution (don't look before trying!)
- `topology.pkt` — Packet Tracer file (add when you build it)
