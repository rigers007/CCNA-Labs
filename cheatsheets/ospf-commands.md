# OSPF — Cheatsheet

## Basic OSPF Configuration
```
router ospf 1
 router-id 1.1.1.1
 network 10.0.0.0 0.0.0.255 area 0
 network 10.0.12.0 0.0.0.3 area 0
 passive-interface G0/0
```

## Default Route Propagation
```
ip route 0.0.0.0 0.0.0.0 <next-hop>
router ospf 1
 default-information originate
```

## Cost Manipulation
```
interface G0/0
 ip ospf cost 100

router ospf 1
 auto-cost reference-bandwidth 10000
```

## DR/BDR Priority
```
interface G0/0
 ip ospf priority 100    ! Higher = more likely DR
 ip ospf priority 0      ! Never DR/BDR
```

## Common Wildcard Masks
| Subnet Mask     | Wildcard Mask   | CIDR |
|-----------------|-----------------|------|
| 255.255.255.252 | 0.0.0.3         | /30  |
| 255.255.255.248 | 0.0.0.7         | /29  |
| 255.255.255.240 | 0.0.0.15        | /28  |
| 255.255.255.224 | 0.0.0.31        | /27  |
| 255.255.255.192 | 0.0.0.63        | /26  |
| 255.255.255.0   | 0.0.0.255       | /24  |

## Verification Commands
```
show ip ospf neighbor
show ip ospf interface brief
show ip route ospf
show ip ospf database
show ip protocols
```
