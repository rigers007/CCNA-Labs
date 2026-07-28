# Lab 26: Standard ACL

🟡 **Difficulty:** Medium | **Module:** 6 — Security

## Objective

Configure a standard ACL to restrict network access.

## Topology

**Devices:** 2 Routers + 2 LANs

```
   [PC 192.168.1.10]--[R1]---WAN---[R2]--[LAN B: 192.168.2.0/24]
```

## Requirements

1. ACL 10: `deny host 192.168.1.10`, `permit any`
2. Apply ACL as close to destination as possible (R2, direction `out`)
3. Test: `.10` should NOT reach LAN B, other PCs should
4. Bonus: rewrite as named ACL `BLOCK-HOST`

## Verification

Submit these outputs after completing the lab:

- `show access-lists`
- `show ip interface (ACL applied)`
- `ping tests`

## 💡 Hint

> Standard ACL: filters source IP only. Place near destination to avoid unwanted blocking.

---

📁 **Structure:**
- `README.md` — Requirements (this file)
- `solution.md` — Solution (don't look before trying!)
- `topology.pkt` — Packet Tracer file (add when you build it)
