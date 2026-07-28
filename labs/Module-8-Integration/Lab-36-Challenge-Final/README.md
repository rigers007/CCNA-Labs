# Lab 36: Final Challenge Lab

🔴 **Difficulty:** Hard | **Module:** 8 — Integration

## Objective

Enterprise + WAN + Security + Wireless — integrates everything.

## Topology

**Devices:** 2 L3 Switches + 2 Access Switches + 2 Edge Routers + ISP + WLC + LAP

```
                        [ISP]
                       /     \
   [R1 edge]----------       ---------[R2 edge]
       |    HSRP+OSPF+NAT+ACL    |
   [L3-SW1]========Po1========[L3-SW2]
       |    SVI routing           |
   [Acc-SW1]                 [Acc-SW2]
   [PCs V10,20,30]          [PCs V10,20,30]
   [WLC]---[LAP]---((WiFi))---[Laptop]
```

## Requirements

1. VLSM: divide `10.0.0.0/16` for 4 VLANs + 2 WANs + mgmt + wireless
2. VLAN 10, 20, 30, 99 + trunk + LACP EtherChannel
3. SVI inter-VLAN routing, DHCP pools, ip helper-address
4. OSPF single-area between L3-SW, R1, R2
5. HSRP with tracking on VLAN gateway
6. Default routes + `default-information originate`
7. PAT overload on edge routers
8. Extended ACL: HTTP/HTTPS only outbound
9. Port Security (sticky, max 2) + PortFast + BPDU Guard
10. Wireless: WLC + LAP, WLAN WPA2-PSK, dedicated VLAN
11. Test: DHCP, inter-VLAN, internet, failover, wireless

## Verification

Submit these outputs after completing the lab:

- `show vlan brief`
- `show etherchannel summary`
- `show ip ospf neighbor`
- `show standby brief`
- `show ip nat translations`
- `show ip dhcp binding`
- `show access-lists`
- `show port-security`
- `Full test matrix`

## 💡 Hint

> This is the final lab — it integrates all 36 labs into one scenario. If you solve it, you're ready for CCNA.

---

📁 **Structure:**
- `README.md` — Requirements (this file)
- `solution.md` — Solution (don't look before trying!)
- `topology.pkt` — Packet Tracer file (add when you build it)
