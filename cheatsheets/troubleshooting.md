# Troubleshooting — Cheatsheet

## Metodologjia: Bottom-Up

### Layer 1 — Physical
```
show interfaces status
show ip interface brief          ! up/down status
show cdp neighbors               ! verify physical connections
```
**Probleme tipike:** cable wrong, interface shutdown, speed/duplex mismatch

### Layer 2 — Data Link
```
show vlan brief                  ! VLAN exists? Port in right VLAN?
show interfaces trunk            ! trunk up? allowed VLANs correct?
show spanning-tree               ! port blocked?
show etherchannel summary        ! EtherChannel formed?
show port-security               ! err-disabled?
show interfaces status err-disabled
```
**Probleme tipike:** VLAN missing, trunk mismatch, native VLAN mismatch, STP blocked, err-disabled

### Layer 3 — Network
```
show ip interface brief          ! IP correct? Interface up?
show ip route                    ! route exists?
show ip ospf neighbor            ! OSPF adjacency formed?
show ip ospf interface brief     ! correct area? passive?
show ip nat translations         ! NAT working?
show access-lists                ! ACL blocking?
```
**Probleme tipike:** wrong IP/mask, missing route, OSPF not forming, ACL blocking, NAT inside/outside reversed

### Layer 7 — Application
```
show ip dhcp binding             ! DHCP working?
show ip dhcp pool                ! pool configured?
show ip ssh                      ! SSH version?
```

## Debugging (use with caution)
```
debug ip ospf adj                ! OSPF adjacency issues
debug ip dhcp server events      ! DHCP problems
debug ip nat                     ! NAT translation issues
undebug all                      ! STOP all debugging
```

## Recovery Commands
```
! err-disabled recovery
interface Fa0/1
 shutdown
 no shutdown

! Or automatic:
errdisable recovery cause psecure-violation
errdisable recovery interval 30

! Clear OSPF process (re-elect DR/BDR)
clear ip ospf process

! Clear NAT translations
clear ip nat translation *
```

## Common Mistakes Checklist
- [ ] `no shutdown` on every interface and SVI
- [ ] VLAN created on ALL switches (not just one)
- [ ] Trunk `allowed vlan` includes all needed VLANs
- [ ] ACL has implicit `deny any` at end — add `permit any` if needed
- [ ] NAT: `ip nat inside` / `outside` on correct interfaces
- [ ] OSPF: wildcard mask (not subnet mask!)
- [ ] DHCP: `ip helper-address` points to DHCP server IP
- [ ] HSRP: virtual IP ≠ real interface IP
- [ ] Static route: next-hop must be reachable
- [ ] `copy run start` to save!
