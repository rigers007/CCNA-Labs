# Lab 15: Multi-VLAN Trunk over EtherChannel

🟡 **Difficulty:** Medium | **Module:** 3 — EtherChannel

## Objective

Combine VLAN, trunk, EtherChannel, and SVI routing.

## Topology

**Devices:** 2 L3 Switches (3560) + 4 PCs (VLAN 10, 20 spread across)

```
   [PC1 V10]--Fa0/1           Fa0/1--[PC3 V10]
   [PC2 V20]--Fa0/2  [SW1]===Po1====[SW2]  Fa0/2--[PC4 V20]
                        ip routing
```

## Requirements

1. Create LACP EtherChannel (Po1) between switches, configure as trunk
2. Create VLAN 10 and 20 on both switches
3. On SW1: SVI VLAN 10 (`10.0.10.1/24`) and VLAN 20 (`10.0.20.1/24`)
4. Enable `ip routing` on SW1
5. Assign PCs: 2 in VLAN 10, 2 in VLAN 20
6. Test ping cross-VLAN and cross-switch

## Verification

Submit these outputs after completing the lab:

- `show etherchannel summary`
- `show ip route (SW1)`
- `show vlan brief`
- `ping cross-VLAN cross-switch`

## 💡 Hint

> Only SW1 needs `ip routing` since it acts as the default gateway.

---

📁 **Structure:**
- `README.md` — Requirements (this file)
- `solution.md` — Solution (don't look before trying!)
- `topology.pkt` — Packet Tracer file (add when you build it)
