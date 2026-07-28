# Lab 05: Trunking Between Switches

🟢 **Difficulty:** Easy | **Module:** 1 — Basics

## Objective

Configure a trunk link between two switches to carry VLAN traffic.

## Topology

**Devices:** 2 Switches (2960) + 4 PCs (2 in VLAN 10, 2 in VLAN 20, spread across switches)

```
        VLAN 10         VLAN 20
   [PC1]--Fa0/1  [PC2]--Fa0/2
              \      /
              [SW1]
                |  Fa0/24 (trunk)
              [SW2]
              /      \
   [PC3]--Fa0/1  [PC4]--Fa0/2
        VLAN 10         VLAN 20
```

## Requirements

1. On both switches, create VLAN 10 (Sales) and VLAN 20 (IT)
2. SW1: Fa0/1 → VLAN 10, Fa0/2 → VLAN 20
3. SW2: Fa0/1 → VLAN 10, Fa0/2 → VLAN 20
4. Link between switches (Fa0/24): configure as trunk (`switchport mode trunk`)
5. Set allowed VLANs on trunk: only 10 and 20
6. Test: PC in VLAN 10 on SW1 should ping PC in VLAN 10 on SW2

## Verification

Submit these outputs after completing the lab:

- `show interfaces trunk`
- `show vlan brief (both switches)`
- `ping tests cross-switch within VLAN`

## 💡 Hint

> A trunk carries traffic from multiple VLANs over a single link. Without a trunk, VLANs stay isolated within each switch.

---

📁 **Structure:**
- `README.md` — Requirements (this file)
- `solution.md` — Solution (don't look before trying!)
- `topology.pkt` — Packet Tracer file (add when you build it)
