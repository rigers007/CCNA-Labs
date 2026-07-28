# Lab 06: Router-on-a-Stick (Inter-VLAN)

🟡 **Difficulty:** Medium | **Module:** 2 — Switching

## Objective

Configure inter-VLAN routing using subinterfaces on a router.

## Topology

**Devices:** 1 Router (2911) + 1 Switch (2960) + 3 PCs (VLAN 10, 20, 30)

```
   [PC1 VLAN10]--Fa0/1
   [PC2 VLAN20]--Fa0/2    [SW1]---Fa0/24(trunk)---G0/0---[R1]
   [PC3 VLAN30]--Fa0/3                              G0/0.10
                                                     G0/0.20
                                                     G0/0.30
```

## Requirements

1. On switch: create VLAN 10, 20, 30 and assign ports to PCs
2. Link switch→router (Fa0/24): configure as trunk
3. On router G0/0: create subinterfaces `.10`, `.20`, `.30`
4. Each subinterface: `encapsulation dot1Q <vlan-id>`, IP as VLAN gateway
5. Activate G0/0 (`no shutdown`)
6. Set PC gateways = corresponding subinterface IP
7. Test ping between VLANs

## Verification

Submit these outputs after completing the lab:

- `show ip interface brief`
- `show vlans (router)`
- `show interfaces trunk (switch)`
- `ping between VLANs`

## 💡 Hint

> Subinterfaces inherit the physical interface status — just `no shutdown` on G0/0 is enough.

---

📁 **Structure:**
- `README.md` — Requirements (this file)
- `solution.md` — Solution (don't look before trying!)
- `topology.pkt` — Packet Tracer file (add when you build it)
