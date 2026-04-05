# 🛡️ TryHackMe — Defensive Security Intro

## Room Info

| Field | Details |
|---|---|
| Platform | TryHackMe |
| Room | Defensive Security Intro |
| Category | Defensive Security |
| Difficulty | Easy |
| Tools Used | SIEM, Firewall, Rate Limiting |

---

## 🧩 Description

An introduction to defensive security operations.
The room covered how a Security Operations Center
(SOC) team detects and responds to an active
attack against an organization in real time.

---

## 🔍 Scenario

An attacker was actively targeting the organization:

- Scanning the network for open ports
- Probing the admin panel
- Attempting to enumerate the infrastructure

The goal was to detect the attack early and
respond before the attacker could find anything
useful.

---

## ⚔️ Response Process

**Step 1 — Detection**

Monitored incoming traffic and identified
suspicious activity from a single IP address:

- Unusually high number of requests
- Port scanning activity detected
- Admin panel being probed repeatedly

**Step 2 — Block Source IP**

Immediately blocked the attacker's IP address
in the firewall rules to cut off their access:
```
Firewall Rule → BLOCK [attacker IP] → ALL TRAFFIC
```

**Step 3 — Rate Limiting**

Implemented rate limiting per IP address with
a timeout to prevent future automated scanning
attempts from any source.

---

## 🚩 Key Takeaway

Acting fast is critical in defensive security.
The faster you detect and respond, the less
damage an attacker can do.

---

## 💡 Lessons Learned

- Defensive security is just as important
  as offensive security
- Early detection = less damage
- Firewall rules are your first line of defense
- Rate limiting protects against automated
  scanning and brute force attacks
- A SOC team monitors, detects and responds
  to threats 24/7
- Speed of response is critical — every
  second counts during an active attack

---

## 🛠️ Concepts Covered

- **SIEM** — Security Information and Event Management
- **Firewall Rules** — Blocking malicious IPs
- **Rate Limiting** — Preventing automated attacks
- **Incident Response** — How to react to active threats
- **SOC Operations** — Role of a defensive security team

---

*Completed on TryHackMe — legal controlled
environment*
