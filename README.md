# 🖧 CCNA Practice Labs

**36 progressive hands-on labs** for consolidating CCNA 200-301 skills — from basic device configuration to full enterprise topologies.

## 📋 About This Repo

This repository contains 36 labs ordered by difficulty, grouped into 8 modules. Each lab includes:

- A clear **objective**
- **Topology** with required devices
- **Step-by-step requirements**
- **Verification commands** to confirm your solution
- A **solution** with explanations (try it yourself first!)

Labs are designed for **Cisco Packet Tracer** (version 8.x+), but most also work in GNS3.

## 🎯 How to Use

1. Read the lab requirements
2. Build the topology yourself in Packet Tracer
3. Configure the devices without looking at the solution
4. Run the verification commands
5. Compare with `solution.md` only after you've tried

### 🌐 Auto-Grader

Paste your `show running-config` into the **[online grader](https://rigers007.github.io/CCNA-Labs/)** to check your work automatically — no Git knowledge required!

## 📊 Progress Tracker

### Module 1 — Basics (Labs 1–5)
| Lab | Title | Difficulty | Status |
|-----|-------|------------|--------|
| 01 | Basic Switch Configuration | 🟢 Easy | ⬜ |
| 02 | Basic Router Configuration | 🟢 Easy | ⬜ |
| 03 | VLSM Subnetting | 🟢 Easy | ⬜ |
| 04 | Basic VLANs | 🟢 Easy | ⬜ |
| 05 | Trunking Between Switches | 🟢 Easy | ⬜ |

### Module 2 — Switching (Labs 6–10)
| Lab | Title | Difficulty | Status |
|-----|-------|------------|--------|
| 06 | Router-on-a-Stick (Inter-VLAN) | 🟡 Medium | ⬜ |
| 07 | Inter-VLAN with SVI (L3 Switch) | 🟡 Medium | ⬜ |
| 08 | STP Verification & Root Bridge | 🟡 Medium | ⬜ |
| 09 | Native VLAN Mismatch & Security | 🟡 Medium | ⬜ |
| 10 | Rapid PVST+ and PortFast | 🟡 Medium | ⬜ |

### Module 3 — EtherChannel & L2 Redundancy (Labs 11–15)
| Lab | Title | Difficulty | Status |
|-----|-------|------------|--------|
| 11 | LACP EtherChannel | 🟡 Medium | ⬜ |
| 12 | PAgP EtherChannel | 🟡 Medium | ⬜ |
| 13 | L3 EtherChannel | 🟡 Medium | ⬜ |
| 14 | EtherChannel Troubleshooting | 🟡 Medium | ⬜ |
| 15 | Multi-VLAN Trunk over EtherChannel | 🟡 Medium | ⬜ |

### Module 4 — Routing (Labs 16–21)
| Lab | Title | Difficulty | Status |
|-----|-------|------------|--------|
| 16 | Static Routes | 🟡 Medium | ⬜ |
| 17 | Default Route & Gateway of Last Resort | 🟡 Medium | ⬜ |
| 18 | Floating Static Route | 🟡 Medium | ⬜ |
| 19 | OSPF Single-Area Basics | 🟡 Medium | ⬜ |
| 20 | OSPF Cost Manipulation & DR/BDR | 🔴 Hard | ⬜ |
| 21 | OSPF + Default Route Propagation | 🔴 Hard | ⬜ |

### Module 5 — Services (Labs 22–25)
| Lab | Title | Difficulty | Status |
|-----|-------|------------|--------|
| 22 | DHCP Server on Router | 🟡 Medium | ⬜ |
| 23 | DHCP Relay (ip helper-address) | 🟡 Medium | ⬜ |
| 24 | Static NAT and Dynamic NAT | 🟡 Medium | ⬜ |
| 25 | PAT (NAT Overload) | 🟡 Medium | ⬜ |

### Module 6 — Security (Labs 26–29)
| Lab | Title | Difficulty | Status |
|-----|-------|------------|--------|
| 26 | Standard ACL | 🟡 Medium | ⬜ |
| 27 | Extended ACL | 🔴 Hard | ⬜ |
| 28 | Port Security | 🟡 Medium | ⬜ |
| 29 | ACL + NAT + DHCP Combined | 🔴 Hard | ⬜ |

### Module 7 — FHRP & High Availability (Labs 30–32)
| Lab | Title | Difficulty | Status |
|-----|-------|------------|--------|
| 30 | Basic HSRP | 🔴 Hard | ⬜ |
| 31 | HSRP with Tracking | 🔴 Hard | ⬜ |
| 32 | HSRP + OSPF + NAT/PAT (Dual-Edge) | 🔴 Hard | ⬜ |

### Module 8 — Integration (Labs 33–36)
| Lab | Title | Difficulty | Status |
|-----|-------|------------|--------|
| 33 | Full Enterprise LAN | 🔴 Hard | ⬜ |
| 34 | WAN + OSPF + NAT Full Topology | 🔴 Hard | ⬜ |
| 35 | Troubleshooting Challenge | 🔴 Hard | ⬜ |
| 36 | Final Challenge Lab | 🔴 Hard | ⬜ |

## 🛠 Requirements

- [Cisco Packet Tracer 8.x+](https://www.netacad.com/courses/packet-tracer) (free with NetAcad account)
- Basic networking knowledge (OSI model, IP addressing)

## 📁 Repository Structure

```
CCNA-Labs/
├── README.md
├── index.html                     ← Auto-Grader (GitHub Pages)
├── labs/
│   ├── Module-1-Basics/
│   │   ├── Lab-01-Switch-Config/
│   │   │   ├── README.md          ← Requirements
│   │   │   ├── solution.md        ← Solution with explanations
│   │   │   └── topology.pkt       ← Packet Tracer file (optional)
│   │   └── ...
│   ├── Module-2-Switching/
│   ├── Module-3-EtherChannel/
│   ├── Module-4-Routing/
│   ├── Module-5-Services/
│   ├── Module-6-Security/
│   ├── Module-7-FHRP/
│   └── Module-8-Integration/
├── cheatsheets/
│   ├── vlan-commands.md
│   ├── ospf-commands.md
│   ├── acl-nat-commands.md
│   └── troubleshooting.md
└── resources/
    └── 36_CCNA_Labs.docx
```

## 📝 Contributing

Found an error or have suggestions? Open an **Issue** or submit a **Pull Request**.

## 📜 License

This material is free for educational use. See [LICENSE](LICENSE) for details.

## 👤 Author

**Rigers Maja** — Master of Sience in Electronic Engineering, focused on networking, cybersecurity & DevOps.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?logo=linkedin)](https://www.linkedin.com/in/rigers-maja)

---

> *"The only way to learn networking is to build networks."*
