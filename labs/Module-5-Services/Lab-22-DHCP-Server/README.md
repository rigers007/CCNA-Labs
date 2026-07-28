# Lab 22: DHCP Server on Router

🟡 **Difficulty:** Medium | **Module:** 5 — Services

## Objective

Configure the router as a DHCP server.

## Topology

**Devices:** 1 Router (2911) + 1 Switch + 4 PCs

```
   [PC1]--[PC2]--[PC3]--[PC4]--[SW1]---G0/0---[R1 DHCP Server]
                                        192.168.10.0/24
```

## Requirements

1. Create DHCP pool `LAN10` for `192.168.10.0/24`
2. Default gateway: `.1`, DNS: `8.8.8.8`
3. `ip dhcp excluded-address 192.168.10.1 192.168.10.10`
4. Set PCs to DHCP (not static)
5. Verify: PCs receive IP automatically

## Verification

Submit these outputs after completing the lab:

- `show ip dhcp binding`
- `show ip dhcp pool`
- `ipconfig /all from PC`

## 💡 Hint

> Excluded-address prevents the router from giving out those IPs — use for gateways, servers, printers.

---

📁 **Structure:**
- `README.md` — Requirements (this file)
- `solution.md` — Solution (don't look before trying!)
- `topology.pkt` — Packet Tracer file (add when you build it)
