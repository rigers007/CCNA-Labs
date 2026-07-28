# Lab 02: Basic Router Configuration — Solution

> ⚠️ **Try it yourself before looking at this!**

## Key Commands

### Interface configuration

```
enable
configure terminal
hostname R1
interface G0/0
 ip address 192.168.1.1 255.255.255.0
 no shutdown
 exit
interface G0/1
 ip address 192.168.2.1 255.255.255.0
 no shutdown
 exit
```

## Successful Verification

- [ ] `show ip interface brief` — OK
- [ ] `show running-config` — OK
- [ ] `ping from PC1 → PC2` — OK

## Notes

Without `no shutdown`, the interface stays administratively down even with an IP configured.
