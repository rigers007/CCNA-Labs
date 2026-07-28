# Lab 24: Static NAT and Dynamic NAT

🟡 **Difficulty:** Medium | **Module:** 5 — Services

## Objective

Configure static NAT for a server and dynamic NAT for PCs.

## Topology

**Devices:** 1 Router + 1 Switch (inside) + ISP. 1 Server + 2 PCs

```
   [Server .100]                          [ISP]
   [PC1]          [SW]---[R1]---outside---[ISP]
   [PC2]              inside
   192.168.1.0/24           203.0.113.0/30
```

## Requirements

1. Server: `192.168.1.100` → static NAT → `203.0.113.10`
2. Dynamic NAT pool: `203.0.113.20 - .30` for PCs
3. ACL 1: permit `192.168.1.0 0.0.0.255`
4. `ip nat inside source list 1 pool NATPOOL`
5. Assign interfaces: `ip nat inside` / `ip nat outside`

## Verification

Submit these outputs after completing the lab:

- `show ip nat translations`
- `show ip nat statistics`
- `ping from server/PC toward ISP`

## 💡 Hint

> Static NAT = permanent 1:1 (for servers). Dynamic NAT = shared pool of addresses (limited).

---

📁 **Structure:**
- `README.md` — Requirements (this file)
- `solution.md` — Solution (don't look before trying!)
- `topology.pkt` — Packet Tracer file (add when you build it)
