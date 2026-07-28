# ACL & NAT — Cheatsheet

## Standard ACL (filter source only)
```
access-list 10 deny host 192.168.1.10
access-list 10 permit any

! Apply NEAR DESTINATION
interface G0/1
 ip access-group 10 out
```

## Named Standard ACL
```
ip access-list standard BLOCK-HOST
 deny host 192.168.1.10
 permit any
```

## Extended ACL (source + destination + port)
```
access-list 100 permit tcp 192.168.1.0 0.0.0.255 host 192.168.2.100 eq 80
access-list 100 permit tcp 192.168.1.0 0.0.0.255 host 192.168.2.100 eq 443
access-list 100 deny ip 192.168.1.0 0.0.0.255 host 192.168.2.100
access-list 100 permit ip any any

! Apply NEAR SOURCE
interface G0/0
 ip access-group 100 in
```

## Static NAT
```
ip nat inside source static 192.168.1.100 203.0.113.10
```

## Dynamic NAT
```
ip nat pool NATPOOL 203.0.113.20 203.0.113.30 netmask 255.255.255.0
access-list 1 permit 192.168.1.0 0.0.0.255
ip nat inside source list 1 pool NATPOOL
```

## PAT (Overload)
```
access-list 1 permit 192.168.1.0 0.0.0.255
ip nat inside source list 1 interface G0/1 overload
```

## Interface Designation
```
interface G0/0
 ip nat inside
interface G0/1
 ip nat outside
```

## Port Security
```
interface Fa0/1
 switchport mode access
 switchport port-security
 switchport port-security maximum 2
 switchport port-security violation shutdown
 switchport port-security mac-address sticky
```

## Verification
```
show access-lists
show ip nat translations
show ip nat statistics
show port-security interface Fa0/1
show port-security address
```
