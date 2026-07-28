# Lab 29: ACL + NAT + DHCP Combined

🔴 **Difficulty:** Hard | **Module:** 6 — Security

## Objective

Realistic scenario: DHCP, PAT, and ACL in one topology.

## Topology

**Devices:** 1 Router (edge) + 1 Switch + 3 PCs + ISP

```
   [PC1][PC2][PC3]---[SW]---[R1 edge]---[ISP]
   DHCP clients         DHCP server
                         PAT overload
                         Extended ACL
```

## Requirements

1. DHCP pool `.50-.100`, gateway `.1`
2. PAT overload toward ISP
3. Extended ACL: allow HTTP/HTTPS, block telnet/SSH toward ISP
4. Apply ACL + NAT
5. Test: DHCP + browsing + telnet blocked

## Verification

Submit these outputs after completing the lab:

- `show ip dhcp binding`
- `show ip nat translations`
- `show access-lists`
- `test suite`

## 💡 Hint

> ACL + NAT order matters: inbound traffic → ACL first, outbound → NAT first. Debug to verify.

---

📁 **Structure:**
- `README.md` — Requirements (this file)
- `solution.md` — Solution (don't look before trying!)
- `topology.pkt` — Packet Tracer file (add when you build it)
