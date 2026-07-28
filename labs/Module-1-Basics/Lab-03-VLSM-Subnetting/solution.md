# Lab 03: VLSM Subnetting — Solution

> ⚠️ **Try it yourself before looking at this!**

## Key Commands

### VLSM Table

| LAN | Hosts | Subnet | Range | Broadcast |
|-----|-------|--------|-------|----------|
| A | 60 | 10.0.0.0/26 | .1 - .62 | .63 |
| B | 30 | 10.0.0.64/27 | .65 - .94 | .95 |
| C | 10 | 10.0.0.96/28 | .97 - .110 | .111 |

## Successful Verification

- [ ] `show ip interface brief` — OK
- [ ] `VLSM table (photo/text)` — OK
- [ ] `ping between LANs` — OK

## Notes

VLSM: always start with the largest subnet (most hosts) and work your way down.
