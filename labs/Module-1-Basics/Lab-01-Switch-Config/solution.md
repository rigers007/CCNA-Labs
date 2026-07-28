# Lab 01: Basic Switch Configuration — Solution

> ⚠️ **Try it yourself before looking at this!**

## Key Commands

### Hostname, banner, passwords

```
enable
configure terminal
hostname SW1
banner motd #Authorized Access Only#
enable secret class
line console 0
 password cisco
 login
 exit
```

### SSH configuration

```
ip domain-name lab.local
crypto key generate rsa general-keys modulus 1024
username admin secret admin123
line vty 0 15
 transport input ssh
 login local
 exit
```

### Save

```
end
copy running-config startup-config
```

## Successful Verification

- [ ] `show running-config` — OK
- [ ] `show ip ssh` — OK
- [ ] `show users` — OK

## Notes

Always set `transport input ssh` (not telnet) for security. RSA key must be at least 1024-bit for SSH v2.
