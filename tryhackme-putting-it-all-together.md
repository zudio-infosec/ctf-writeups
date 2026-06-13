# Putting It All Together - TryHackMe Writeup

**Room:** Putting it all together  
**Difficulty:** Easy  
**Category:** Web Basics  
**Date Completed:** 2025  
**Platform:** TryHackMe

## Challenge Description
Learn how all the individual components of the web work together to bring you access to your favourite web sites.

## Components Covered

### 1. DNS (Domain Name System)
- Translates domain names to IP addresses
- Types of DNS records: A, AAAA, CNAME, MX, TXT
- DNS resolution process

### 2. Web Servers
- Apache, Nginx
- Virtual hosts
- Request handling

### 3. Databases
- SQL (MySQL, PostgreSQL)
- NoSQL (MongoDB)
- Data storage and retrieval

### 4. Programming Languages
- Backend: PHP, Python, Node.js, Ruby
- Frameworks

### 5. APIs
- REST APIs
- JSON data format
- Endpoint security

## How It All Connects

```
User Browser → DNS → IP Address → Web Server → Application → Database
     ↑                                                           │
     └──────────────────── Response ←─────────────────────────────┘
```

### Flow:
1. User enters domain in browser
2. DNS resolves to IP
3. Browser sends HTTP request
4. Web server processes request
5. Application logic executes
6. Database queried if needed
7. Response returned to user

## Learning Points
- Full stack understanding matters
- Each component has security implications
- Debugging requires knowing the flow

---
*Writeup by @zudio-infosec*  
*For more: github.com/zudio-infosec/ctf-writeups*