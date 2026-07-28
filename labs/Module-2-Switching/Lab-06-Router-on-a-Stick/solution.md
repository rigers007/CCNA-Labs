# Lab 06: Router-on-a-Stick (Inter-VLAN) — Solution

> ⚠️ **Try it yourself before looking at this!**

## Key Commands

### Subinterface config on R1

```
interface G0/0
 no shutdown
interface G0/0.10
 encapsulation dot1Q 10
 ip address 10.0.10.1 255.255.255.0
interface G0/0.20
 encapsulation dot1Q 20
 ip address 10.0.20.1 255.255.255.0
interface G0/0.30
 encapsulation dot1Q 30
 ip address 10.0.30.1 255.255.255.0
```

## Successful Verification

- [ ] `show ip interface brief` — OK
- [ ] `show vlans (router)` — OK
- [ ] `show interfaces trunk (switch)` — OK
- [ ] `ping between VLANs` — OK

## Notes

Subinterfaces inherit the physical interface status — just `no shutdown` on G0/0 is enough.
