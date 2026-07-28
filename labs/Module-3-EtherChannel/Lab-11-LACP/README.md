# Lab 11: LACP EtherChannel

🟡 **Difficulty:** Medium | **Module:** 3 — EtherChannel

## Objective

Configure LACP EtherChannel between two switches.

## Topology

**Devices:** 2 Switches (2960) with 2 physical links + 2 PCs

```
   [PC1]--Fa0/1--[SW1]===Po1====[SW2]--Fa0/1--[PC2]
                    Fa0/23 (active)  Fa0/23 (passive)
                    Fa0/24 (active)  Fa0/24 (passive)
```

## Requirements

1. Connect SW1↔SW2 with Fa0/23 and Fa0/24
2. SW1: `channel-group 1 mode active` (Fa0/23-24)
3. SW2: `channel-group 1 mode passive` (Fa0/23-24)
4. Configure Port-Channel 1 as trunk with allowed VLANs 10, 20
5. Create VLANs and assign PCs
6. Verify EtherChannel is Up

## Verification

Submit these outputs after completing the lab:

- `show etherchannel summary`
- `show etherchannel port-channel`
- `show interfaces trunk`

## 💡 Hint

> LACP: active+active or active+passive works. passive+passive does NOT work.

---

📁 **Structure:**
- `README.md` — Requirements (this file)
- `solution.md` — Solution (don't look before trying!)
- `topology.pkt` — Packet Tracer file (add when you build it)
