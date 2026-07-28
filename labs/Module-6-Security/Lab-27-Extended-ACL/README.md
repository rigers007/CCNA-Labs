# Lab 27: Extended ACL

🔴 **Difficulty:** Hard | **Module:** 6 — Security

## Objective

Configure an extended ACL with port-specific filtering.

## Topology

**Devices:** 1 Router + 2 LANs + 1 Server (HTTP/HTTPS)

```
   [PC VLAN10]--[R1]--[Server .100 HTTP/HTTPS]
   192.168.1.0/24    192.168.2.0/24
```

## Requirements

1. Extended ACL 100:
2.   permit VLAN10 → server only ports 80 and 443
3.   deny VLAN10 → server everything else
4.   permit all other traffic
5. Apply as close to source as possible (direction `in`)
6. Test: HTTP/HTTPS works, ping/telnet/SSH doesn't

## Verification

Submit these outputs after completing the lab:

- `show access-lists (hit counters)`
- `show ip interface`
- `test HTTP vs ping vs telnet`

## 💡 Hint

> Extended ACL: filters source, destination, protocol, and port. Place near source for efficiency.

---

📁 **Structure:**
- `README.md` — Requirements (this file)
- `solution.md` — Solution (don't look before trying!)
- `topology.pkt` — Packet Tracer file (add when you build it)
