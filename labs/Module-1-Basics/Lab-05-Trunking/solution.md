# Lab 05: Trunking Between Switches — Solution

> ⚠️ **Try it yourself before looking at this!**

## Key Commands

### Trunk configuration

```
! On both SW1 and SW2:
interface Fa0/24
 switchport mode trunk
 switchport trunk allowed vlan 10,20
 exit
```

## Successful Verification

- [ ] `show interfaces trunk` — OK
- [ ] `show vlan brief (both switches)` — OK
- [ ] `ping tests cross-switch within VLAN` — OK

## Notes

A trunk carries traffic from multiple VLANs over a single link. Without a trunk, VLANs stay isolated within each switch.
