# Lab 34: WAN + OSPF + NAT Full Topology

🔴 **Difficulty:** Hard | **Module:** 8 — Integration

## Objective

WAN topology with OSPF, NAT, ACL, DHCP relay.

## Topology

**Devices:** 3 Routers (HQ, Branch, ISP) + 2 Switches + 4 PCs

```
   [HQ LAN]--[R-HQ]---OSPF---[R-Branch]--[Branch LAN]
                  \
                   ---static---[ISP]
   HQ: DHCP server, PAT, ACL, default-info originate
```

## Requirements

1. HQ: `10.10.0.0/16` (VLSM into 2 VLANs), Branch: `10.20.0.0/16`
2. OSPF area 0 HQ↔Branch, static HQ→ISP
3. HQ: `default-information originate`
4. PAT overload HQ → ISP
5. Extended ACL: block telnet/SSH toward ISP, allow HTTP/HTTPS
6. DHCP relay: HQ as server for Branch too (`ip helper` on Branch router)
7. Test: Branch PC gets DHCP from HQ, browses ISP, can't telnet ISP

## Verification

Submit these outputs after completing the lab:

- `show ip ospf neighbor`
- `show ip route ospf`
- `show ip nat translations`
- `show ip dhcp binding`
- `show access-lists`
- `full test matrix`

## 💡 Hint

> This scenario simulates a small company with HQ + Branch. Ideal for practical exam prep.

---

📁 **Structure:**
- `README.md` — Requirements (this file)
- `solution.md` — Solution (don't look before trying!)
- `topology.pkt` — Packet Tracer file (add when you build it)
