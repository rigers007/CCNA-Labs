# Lab 01: Basic Switch Configuration

🟢 **Difficulty:** Easy | **Module:** 1 — Basics

## Objective

Configure hostname, banner, passwords, and SSH on a switch.

## Topology

**Devices:** 1 Switch (2960) + 1 PC with console cable

```
   [PC] ---console--- [SW1]
```

## Requirements

1. Change hostname to `SW1`
2. Set MOTD banner: `Authorized Access Only`
3. Configure enable secret: `class` and console password: `cisco`
4. Configure VTY lines 0-15 with password `cisco` and `transport input ssh`
5. Create domain name `lab.local` and generate RSA key 1024-bit
6. Create user `admin` with secret `admin123`, set `login local` on VTY
7. Save configuration with `copy run start`

## Verification

Submit these outputs after completing the lab:

- `show running-config`
- `show ip ssh`
- `show users`

## 💡 Hint

> Always set `transport input ssh` (not telnet) for security. RSA key must be at least 1024-bit for SSH v2.

---

📁 **Structure:**
- `README.md` — Requirements (this file)
- `solution.md` — Solution (don't look before trying!)
- `topology.pkt` — Packet Tracer file (add when you build it)
