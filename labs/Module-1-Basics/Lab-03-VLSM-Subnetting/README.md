# Lab 03: VLSM Subnetting

🟢 **Difficulty:** Easy | **Module:** 1 — Basics

## Objective

Divide a /24 network into different subnets using VLSM.

## Topology

**Devices:** 1 Router (2911) + 3 segments: LAN A (60 hosts), LAN B (30 hosts), LAN C (10 hosts). Base network: 10.0.0.0/24

```
   [LAN A: 60 hosts] ---G0/0--- [R1] ---G0/1--- [LAN B: 30 hosts]
                                  |
                                G0/2
                                  |
                          [LAN C: 10 hosts]
```

## Requirements

1. Calculate VLSM subnets on paper: LAN A (/26), LAN B (/27), LAN C (/28)
2. Configure 3 router interfaces with the first usable IP of each subnet
3. Set PCs with correct IPs within each subnet
4. Test ping between segments

## Verification

Submit these outputs after completing the lab:

- `show ip interface brief`
- `VLSM table (photo/text)`
- `ping between LANs`

## 💡 Hint

> VLSM: always start with the largest subnet (most hosts) and work your way down.

---

📁 **Structure:**
- `README.md` — Requirements (this file)
- `solution.md` — Solution (don't look before trying!)
- `topology.pkt` — Packet Tracer file (add when you build it)
