# Lab 23: DHCP Relay (ip helper-address)

🟡 **Difficulty:** Medium | **Module:** 5 — Services

## Objective

Configure DHCP relay when the DHCP server is on a different subnet.

## Topology

**Devices:** 2 Routers + 1 Switch. R1=DHCP server, R2=relay

```
   [R1 DHCP]---10.0.0.0/30---[R2]---G0/1---[SW]---[PC1][PC2]
                                ip helper       192.168.20.0/24
```

## Requirements

1. R1: DHCP pool for `192.168.20.0/24` (subnet behind R2)
2. WAN: `10.0.0.0/30`
3. R2 G0/1 (toward PCs): `ip helper-address 10.0.0.1`
4. Set PCs to DHCP
5. Verify: PCs receive IP from R1's pool

## Verification

Submit these outputs after completing the lab:

- `show ip dhcp binding (R1)`
- `ipconfig /all (PC)`

## 💡 Hint

> DHCP Discover is broadcast — it doesn't cross routers. `ip helper-address` converts it to unicast toward the server.

---

📁 **Structure:**
- `README.md` — Requirements (this file)
- `solution.md` — Solution (don't look before trying!)
- `topology.pkt` — Packet Tracer file (add when you build it)
