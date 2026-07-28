# Lab 04: Basic VLANs — Solution

> ⚠️ **Try it yourself before looking at this!**

## Key Commands

### VLAN creation & port assignment

```
enable
configure terminal
vlan 10
 name Sales
vlan 20
 name IT
exit
interface range Fa0/1-2
 switchport mode access
 switchport access vlan 10
 exit
interface range Fa0/3-4
 switchport mode access
 switchport access vlan 20
 exit
```

## Successful Verification

- [ ] `show vlan brief` — OK
- [ ] `show interfaces switchport (Fa0/1 and Fa0/3)` — OK
- [ ] `ping tests` — OK

## Notes

Ping between VLANs won't work without inter-VLAN routing (Labs 6-7). This is expected behavior.
