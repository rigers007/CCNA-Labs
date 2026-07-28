# Lab 25: PAT (NAT Overload)

🟡 **Difficulty:** Medium | **Module:** 5 — Services

## Objective

Configure PAT using the outside interface.

## Topology

**Devices:** 1 Router + 1 Switch + 3 PCs + ISP

```
   [PC1][PC2][PC3]---[SW]---[R1]---outside---[ISP]
                         inside    G0/1
   192.168.1.0/24             203.0.113.0/30
```

## Requirements

1. ACL 1: `permit 192.168.1.0 0.0.0.255`
2. `ip nat inside source list 1 interface G0/1 overload`
3. Assign `ip nat inside`/`outside`
4. All 3 PCs should reach ISP simultaneously
5. Verify: same outside IP, different ports

## Verification

Submit these outputs after completing the lab:

- `show ip nat translations`
- `show ip nat statistics`
- `simultaneous ping from 3 PCs`

## 💡 Hint

> PAT (overload) = many hosts share 1 public IP, differentiated by port numbers. This is the most common NAT type.

---

📁 **Structure:**
- `README.md` — Requirements (this file)
- `solution.md` — Solution (don't look before trying!)
- `topology.pkt` — Packet Tracer file (add when you build it)
