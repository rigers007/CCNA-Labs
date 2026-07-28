# Lab 14: EtherChannel Troubleshooting

🟡 **Difficulty:** Medium | **Module:** 3 — EtherChannel

## Objective

Diagnose and fix an EtherChannel that won't form.

## Topology

**Devices:** 2 Switches (2960) with 2 physical links

```
   [SW1]---X---[SW2]   ← EtherChannel won't form!
```

## Requirements

1. SW1: `mode active`, SW2: `mode desirable` → won't work (LACP vs PAgP!)
2. Verify — explain WHY it won't form
3. Fix: set SW2 to `mode active` or `passive`
4. Verify it forms
5. Bug #2: set different speeds (100 vs auto) — verify the effect
6. Fix speeds and verify

## Verification

Submit these outputs after completing the lab:

- `show etherchannel summary (before/after)`
- `Explanation of causes`

## 💡 Hint

> EtherChannel requires: same protocol (LACP or PAgP), speed, duplex, VLAN, and trunk mode on all ports.

---

📁 **Structure:**
- `README.md` — Requirements (this file)
- `solution.md` — Solution (don't look before trying!)
- `topology.pkt` — Packet Tracer file (add when you build it)
