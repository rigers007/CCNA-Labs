# Lab 33: Full Enterprise LAN

🔴 **Difficulty:** Hard | **Module:** 8 — Integration

## Objective

Enterprise LAN with VLAN, EtherChannel, SVI, DHCP, Port Security.

## Topology

**Devices:** 2 L3 Switches + 2 Access Switches + 8 PCs (4 VLANs)

```
   [L3-SW1]===Po1(trunk)===[L3-SW2]
      |  trunk                |  trunk
   [Acc-SW1]              [Acc-SW2]
   PC×4 (V10,20,30,99)   PC×4 (V10,20,30,99)
```

## Requirements

1. VLAN 10 (Sales), 20 (IT), 30 (HR), 99 (Mgmt)
2. LACP EtherChannel (Po1, trunk) between L3 switches
3. Trunk links from L3 to access switches
4. SVI routing on SW-L3-1
5. DHCP pools for VLAN 10, 20, 30
6. PortFast + BPDU Guard on access ports
7. Port Security (sticky, max 2)
8. Test DHCP + inter-VLAN + cross-switch

## Verification

Submit these outputs after completing the lab:

- `show vlan brief`
- `show etherchannel summary`
- `show ip dhcp binding`
- `show ip route`
- `show port-security`
- `ping matrix`

## 💡 Hint

> This lab tests whether you can tie technologies together. Start with VLAN+trunk, then EtherChannel, then routing.

---

📁 **Structure:**
- `README.md` — Requirements (this file)
- `solution.md` — Solution (don't look before trying!)
- `topology.pkt` — Packet Tracer file (add when you build it)
