# Nmap Live Host Discovery - TryHackMe Writeup

**Room:** Nmap Live Host Discovery  
**Difficulty:** Medium  
**Category:** Network Scanning  
**Date Completed:** 2025  
**Platform:** TryHackMe

## Challenge Description
Learn how to use Nmap to discover live hosts using ARP, ICMP, and TCP/UDP ping scan.

## Nmap Basics

### Installation
```bash
sudo apt-get install nmap
```

### Basic Syntax
```bash
nmap [Scan Type(s)] [Options] {target specification}
```

## Host Discovery Methods

### 1. ARP Scan (Local Network)
```bash
nmap -PR 192.168.1.0/24
```
- Most accurate on local networks
- Requires root/sudo

### 2. ICMP Echo (Ping)
```bash
nmap -PE 192.168.1.1-254
nmap -PP 192.168.1.0/24  # Timestamp
nmap -PM 192.168.1.0/24  # Netmask
```

### 3. TCP/UDP Ping
```bash
nmap -PS 80,443 192.168.1.1   # SYN ping
nmap -PA 80,443 192.168.1.1  # ACK ping
nmap -PU 53,161 192.168.1.1  # UDP ping
```

### 4. Combined Scans
```bash
nmap -sn 192.168.1.0/24  # Skip port scan
nmap -sP 192.168.1.0/24  # Ping scan only
```

## Common Options
- `-sn` - Ping scan (no port scan)
- `-Pn` - Skip host discovery
- `-n` - No DNS resolution
- `-R` - Always resolve DNS
- `-oA` - Output all formats

## Practical Examples
```bash
# Discover live hosts
nmap -sn 192.168.1.0/24

# Quick scan with ping
nmap -sP 10.0.0.1-254

# Scan with specific interface
nmap -e eth0 -PR 192.168.1.0/24
```

## Learning Points
- ARP is most reliable on local networks
- ICMP often blocked by firewalls
- Combine methods for best results

---
*Writeup by @zudio-infosec*  
*For more: github.com/zudio-infosec/ctf-writeups*