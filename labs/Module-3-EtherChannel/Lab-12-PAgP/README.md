# Lab 12: PAgP EtherChannel

🟡 **Difficulty:** Medium | **Module:** 3 — EtherChannel

## Objective

Configure PAgP (Cisco proprietary) EtherChannel.

## Topology

**Devices:** 2 Switches (2960) with 2 physical links

```
   [SW1]===Po2====[SW2]
     Fa0/21 (desirable)  Fa0/21 (auto)
     Fa0/22 (desirable)  Fa0/22 (auto)
```

## Requirements

1. Connect SW1↔SW2 with Fa0/21 and Fa0/22
2. SW1: `channel-group 2 mode desirable`
3. SW2: `channel-group 2 mode auto`
4. Configure Po2 as trunk
5. Verify Po2 is Up and protocol is PAgP

## Verification

Submit these outputs after completing the lab:

- `show etherchannel summary`
- `show etherchannel protocol`

## 💡 Hint

> PAgP: desirable+desirable or desirable+auto works. auto+auto does NOT work. PAgP only works with Cisco devices.

---

📁 **Structure:**
- `README.md` — Requirements (this file)
- `solution.md` — Solution (don't look before trying!)
- `topology.pkt` — Packet Tracer file (add when you build it)
