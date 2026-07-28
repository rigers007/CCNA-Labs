# Lab 29: ACL + NAT + DHCP Combined — Solution

> ⚠️ **Try it yourself before looking at this!**

## Key Commands

*Solution will be added after completing the lab.*

## Successful Verification

- [ ] `show ip dhcp binding` — OK
- [ ] `show ip nat translations` — OK
- [ ] `show access-lists` — OK
- [ ] `test suite` — OK

## Notes

ACL + NAT order matters: inbound traffic → ACL first, outbound → NAT first. Debug to verify.
