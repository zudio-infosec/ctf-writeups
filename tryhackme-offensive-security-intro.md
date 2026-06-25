# 🔐 TryHackMe — Offensive Security Intro

## Room Info

| Field | Details |
|---|---|
| Platform | TryHackMe |
| Room | Offensive Security Intro |
| Category | Offensive Security |
| Difficulty | Easy |
| Tools Used | dirb |

---

## 🧩 Description

An introduction to offensive security using a 
simulated banking application called FakeBank. 
The goal was to find a hidden page on the web 
application and perform an unauthorized transfer 
to demonstrate how attackers exploit web apps.

---

## 🔍 Reconnaissance

The target was a browser-based banking app — 
FakeBank. My account number was `8881`.

The visible pages didn't reveal anything 
interesting so I moved to directory enumeration 
to find hidden pages.

---

## ⚔️ Attack Process

**Step 1 — Directory Enumeration with dirb**

Ran dirb against the target to discover 
hidden directories:
```bash
dirb http://fakebank.thm
```

dirb found two hidden pages:
```
/images
/bank-transfer
```

**Step 2 — Accessing /bank-transfer**

Navigated to `/bank-transfer` in the browser.
Found an internal bank transfer form that 
was not linked anywhere on the site — 
completely hidden from normal users.

**Step 3 — Transferring Funds**

Used the hidden transfer form to deposit 
money into account `8881`.

The application processed the transfer 
without any authentication check — 
a critical security vulnerability.

---

## 🚩 Flag
```
BANK HACKED
```

---

## 💡 Lessons Learned

- Hidden pages are not secure just because 
  they are not linked anywhere
- Directory enumeration with tools like 
  `dirb` or `gobuster` can reveal sensitive 
  pages very quickly
- Web applications must enforce authentication 
  on ALL sensitive endpoints — not just 
  visible ones
- Security through obscurity is not real security
- Always test every discovered endpoint 
  for access control vulnerabilities

---

## 🛠️ Tools Used

- **dirb** — Directory and file enumeration
- **Browser** — Accessing discovered endpoints

---

*Completed on TryHackMe — legal controlled 
environment*
