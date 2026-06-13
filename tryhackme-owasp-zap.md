# Introduction to OWASP ZAP - TryHackMe Writeup

**Room:** Introduction to OWASP ZAP  
**Difficulty:** Easy  
**Category:** Web Security  
**Date Completed:** 2025  
**Platform:** TryHackMe

## Challenge Description
Learn how to use OWASP ZAP from the ground up. An alternative to BurpSuite.

## What is OWASP ZAP?
OWASP ZAP (Zed Attack Proxy) is a free, open-source web application security scanner. It's designed to find vulnerabilities in web applications.

## Key Features
- Proxy-based traffic interception
- Automated vulnerability scanning
- Passive scanning
- Active scanning (attacks the application)
- Fuzzing
- Spider functionality

## Getting Started

### 1. Setting Up Proxy
```
Tools > Options > Local Proxy
Set port (e.g., 8080)
```

### 2. Browser Configuration
Configure browser to use ZAP as proxy (127.0.0.1:8080)

### 3. Key Functions
- **Spider:** Discovers pages and URLs
- **Active Scan:** Tests for vulnerabilities
- **Passive Scan:** Monitors traffic automatically
- **Fuzzer:** Tests for injection points

## Basic Workflow
1. Configure browser proxy
2. Visit target website
3. Review passive scan results
4. Run Spider
5. Run Active Scan
6. Review and export findings

## Tools Used
- OWASP ZAP
- Browser (configured as proxy)

## Learning Points
- ZAP vs BurpSuite: ZAP is free and open-source
- Always get permission before scanning
- Passive scanning is safe, active scanning is aggressive

---
*Writeup by @zudio-infosec*  
*For more: github.com/zudio-infosec/ctf-writeups*