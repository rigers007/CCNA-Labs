# Lab 02: Basic Router Configuration

🟢 **Difficulty:** Easy | **Module:** 1 — Basics

## Objective

Configure hostname, interfaces, and IP addressing on a router.

## Topology

**Devices:** 1 Router (2911) + 2 PCs

```
   [PC1] ---G0/0--- [R1] ---G0/1--- [PC2]
   .10/24              .1    .1              .10/24
   192.168.1.0/24            192.168.2.0/24
```

## Requirements

1. Change hostname to `R1`
2. Configure `G0/0` with IP `192.168.1.1/24` and `G0/1` with IP `192.168.2.1/24`
3. Activate both interfaces (`no shutdown`)
4. Set PC1: IP `192.168.1.10/24`, gateway `.1`
5. Set PC2: IP `192.168.2.10/24`, gateway `.1`
6. Set MOTD, enable secret, console/VTY passwords
7. Test ping from PC1 to PC2

## Verification

Submit these outputs after completing the lab:

- `show ip interface brief`
- `show running-config`
- `ping from PC1 → PC2`

## 💡 Hint

> Without `no shutdown`, the interface stays administratively down even with an IP configured.

---

📁 **Structure:**
- `README.md` — Requirements (this file)
- `solution.md` — Solution (don't look before trying!)
- `topology.pkt` — Packet Tracer file (add when you build it)
