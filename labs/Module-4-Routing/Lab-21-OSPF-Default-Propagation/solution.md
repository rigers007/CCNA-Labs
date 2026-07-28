# Lab 21: OSPF + Default Route Propagation — Solution

> ⚠️ **Try it yourself before looking at this!**

## Key Commands

*Solution will be added after completing the lab.*

## Successful Verification

- [ ] `show ip route ospf (R1, R3 — look for O*E2)` — OK
- [ ] `show ip ospf database (external LSA)` — OK
- [ ] `ping end-to-end` — OK

## Notes

`always` propagates even when R2 itself doesn't have an active default route. Without `always`, the route must exist.
