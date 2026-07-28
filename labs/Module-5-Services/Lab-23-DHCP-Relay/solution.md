# Lab 23: DHCP Relay (ip helper-address) — Solution

> ⚠️ **Try it yourself before looking at this!**

## Key Commands

*Solution will be added after completing the lab.*

## Successful Verification

- [ ] `show ip dhcp binding (R1)` — OK
- [ ] `ipconfig /all (PC)` — OK

## Notes

DHCP Discover is broadcast — it doesn't cross routers. `ip helper-address` converts it to unicast toward the server.
