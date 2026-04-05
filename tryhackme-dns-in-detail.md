# 🌐 TryHackMe — DNS in Detail

## Room Info

| Field | Details |
|---|---|
| Platform | TryHackMe |
| Room | DNS in Detail |
| Category | Networking |
| Difficulty | Easy |
| Tools Used | nslookup, dig |

---

## 🧩 Description

A detailed room covering how the Domain Name
System (DNS) works, its different record types,
domain structure, and how responses are cached
locally.

---

## 📚 Key Concepts Learned

### Domain Structure
```
subdomain.secondlevel.TLD
    blog  .  google  .com
```

| Part | Example | Meaning |
|---|---|---|
| TLD | `.com` `.org` `.uk` | Top Level Domain |
| Second Level | `google` | The actual domain name |
| Subdomain | `blog` | Division of the domain |
| Root Domain | `.` | The invisible dot at the end |

---

### DNS Record Types

| Record | Purpose |
|---|---|
| `A` | Maps domain to IPv4 address |
| `AAAA` | Maps domain to IPv6 address |
| `CNAME` | Points domain to another domain |
| `MX` | Mail server for the domain |
| `TXT` | Text records — used for verification |

---

### How DNS Resolution Works
```
You type → google.com
        ↓
Check local cache first
        ↓
Ask Recursive DNS Server
        ↓
Ask Root DNS Server → points to .com TLD
        ↓
Ask TLD Server → points to google.com nameserver
        ↓
Ask Authoritative Server → returns IP address
        ↓
IP returned → cached locally with TTL
        ↓
Browser connects to IP
```

---

### TTL — Time To Live

- TTL is a value in seconds
- Tells your system how long to cache the DNS response
- Example: TTL = 300 means cache for 5 minutes
- After TTL expires → system asks DNS again
- Lower TTL = more up to date but more DNS requests
- Higher TTL = faster but might be outdated

---

## 💡 Lessons Learned

- DNS is like the internet's phone book —
  converts names to IP addresses
- DNS responses are cached locally to
  speed up browsing
- TTL controls how long a cache entry lives
- Understanding DNS is critical for
  both offensive and defensive security
- Tools like `dig` and `nslookup` are used
  to query DNS records manually

---

## 🛠️ Tools Used

- **dig** — DNS lookup tool
- **nslookup** — Query DNS records

---

*Completed on TryHackMe — legal controlled
environment*
