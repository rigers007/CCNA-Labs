# Lab 35: Troubleshooting Challenge

🔴 **Difficulty:** Hard | **Module:** 8 — Integration

## Objective

Pre-built topology with 8 hidden errors — find and fix them.

## Topology

**Devices:** 2 Routers + 2 Switches + 4 PCs

```
   Full topology with VLAN, trunk, OSPF, DHCP, ACL, NAT
   8 INTENTIONAL ERRORS — find each one!
```

## Requirements

1. You'll receive running-configs with 8 intentional errors:
2. 1. Trunk mismatch
3. 2. VLAN missing on one switch
4. 3. Wrong OSPF network statement
5. 4. DHCP excluded-address error
6. 5. Inverted ACL logic
7. 6. NAT inside/outside reversed
8. 7. SVI without `no shutdown`
9. 8. Missing default route
10. Identify each error and write the fix commands

## Verification

Submit these outputs after completing the lab:

- `List of 8 errors with explanations`
- `Corrective commands for each`

## 💡 Hint

> Request the broken configs from me (Claude) when you're ready — I'll send them with hidden errors.

---

📁 **Structure:**
- `README.md` — Requirements (this file)
- `solution.md` — Solution (don't look before trying!)
- `topology.pkt` — Packet Tracer file (add when you build it)
