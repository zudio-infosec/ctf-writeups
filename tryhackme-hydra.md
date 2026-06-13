# Hydra - TryHackMe Writeup

**Room:** Hydra  
**Difficulty:** Easy  
**Category:** Password Cracking  
**Date Completed:** 2025  
**Platform:** TryHackMe

## Challenge Description
Learn about and use Hydra, a fast network logon cracker, to bruteforce and obtain a website's credentials.

## Steps

### 1. Introduction to Hydra
- Learned about Hydra tool and its capabilities
- Understanding the syntax and options

### 2. Basic Hydra Commands
```bash
hydra -l username -p passwordlist.txt targetIP http-post-form
```

### 3. Service-specific Attacks
- HTTP login forms
- SSH authentication
- FTP brute force

### 4. Common Flags Used
- `-l` = login (single username)
- `-L` = login list
- `-p` = password (single password)
- `-P` = password list
- `-t` = tasks (parallel connections)
- `-V` = verbose output

### 5. Examples
```bash
# SSH attack
hydra -l admin -P rockyou.txt 192.168.1.100 ssh

# HTTP POST form
hydra -l admin -P rockyou.txt 192.168.1.100 http-post-form "/login:username=^USER^&password=^PASS^:F=incorrect"
```

## Tools Used
- Hydra
- Wordlists (rockyou.txt)
- Various wordlists

## Learning Points
- Hydra is powerful but use responsibly
- Always use wordlists efficiently
- Rate limiting can prevent brute force attacks

---
*Writeup by @zudio-infosec*  
*For more: github.com/zudio-infosec/ctf-writeups*