# Lab 07: Inter-VLAN with SVI (L3 Switch)

🟡 **Difficulty:** Medium | **Module:** 2 — Switching

## Objective

Configure inter-VLAN routing using SVIs on a multilayer switch.

## Topology

**Devices:** 1 L3 Switch (3560) + 4 PCs (VLAN 10, 20, 30, 99)

```
   [PC1 VLAN10]--Fa0/1
   [PC2 VLAN20]--Fa0/2    [L3-SW1]  ← ip routing enabled
   [PC3 VLAN30]--Fa0/3      SVI: vlan10 .1, vlan20 .1, vlan30 .1, vlan99 .1
   [Admin VLAN99]--Fa0/4
```

## Requirements

1. Enable `ip routing` on the switch
2. Create VLAN 10, 20, 30, 99
3. Create SVI for each VLAN (`interface vlan X`) with gateway IP
4. Assign access ports to PCs
5. VLAN 99: management VLAN — assign one port for admin PC
6. Test ping between all VLANs

## Verification

Submit these outputs after completing the lab:

- `show ip interface brief`
- `show ip route`
- `show vlan brief`
- `ping cross-VLAN`

## 💡 Hint

> SVI routing is more efficient than router-on-a-stick because traffic never leaves the switch.

---

📁 **Structure:**
- `README.md` — Requirements (this file)
- `solution.md` — Solution (don't look before trying!)
- `topology.pkt` — Packet Tracer file (add when you build it)
