# Lab 04: Basic VLANs

🟢 **Difficulty:** Easy | **Module:** 1 — Basics

## Objective

Create VLANs and assign ports.

## Topology

**Devices:** 1 Switch (2960) + 4 PCs (2 in VLAN 10, 2 in VLAN 20)

```
   [PC1]--Fa0/1    [PC2]--Fa0/2     ← VLAN 10 (Sales)
              \      /
              [SW1]
              /      \
   [PC3]--Fa0/3    [PC4]--Fa0/4     ← VLAN 20 (IT)
```

## Requirements

1. Create VLAN 10 named `Sales` and VLAN 20 named `IT`
2. Assign Fa0/1, Fa0/2 to VLAN 10 (`switchport mode access`)
3. Assign Fa0/3, Fa0/4 to VLAN 20 (`switchport mode access`)
4. Set IPs: VLAN10 PCs `10.0.10.x/24`, VLAN20 PCs `10.0.20.x/24`
5. Test: ping within VLAN should work, between VLANs should not

## Verification

Submit these outputs after completing the lab:

- `show vlan brief`
- `show interfaces switchport (Fa0/1 and Fa0/3)`
- `ping tests`

## 💡 Hint

> Ping between VLANs won't work without inter-VLAN routing (Labs 6-7). This is expected behavior.

---

📁 **Structure:**
- `README.md` — Requirements (this file)
- `solution.md` — Solution (don't look before trying!)
- `topology.pkt` — Packet Tracer file (add when you build it)
