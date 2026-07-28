# VLAN & Trunking — Cheatsheet

## VLAN Creation
```
vlan 10
 name Sales
```

## Port Assignment
```
interface Fa0/1
 switchport mode access
 switchport access vlan 10
```

## Trunk Configuration
```
interface Fa0/24
 switchport mode trunk
 switchport trunk allowed vlan 10,20,30
 switchport trunk native vlan 99
```

## Inter-VLAN: Router-on-a-Stick
```
interface G0/0.10
 encapsulation dot1Q 10
 ip address 10.0.10.1 255.255.255.0
```

## Inter-VLAN: SVI (L3 Switch)
```
ip routing
interface vlan 10
 ip address 10.0.10.1 255.255.255.0
 no shutdown
```

## EtherChannel (LACP)
```
interface range Fa0/23-24
 channel-group 1 mode active
interface Po1
 switchport mode trunk
 switchport trunk allowed vlan 10,20
```

## Verification Commands
```
show vlan brief
show interfaces trunk
show interfaces switchport
show etherchannel summary
show spanning-tree
```
