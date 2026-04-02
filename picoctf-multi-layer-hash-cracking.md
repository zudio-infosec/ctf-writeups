# 🔐 PicoCTF — Multi-Layer Hash Cracking

## Challenge Info

| Field | Details |
|---|---|
| Platform | PicoCTF |
| Category | Cryptography |
| Difficulty | Easy/Medium |
| Tools Used | SSH, Hash-identifier, John the Ripper / CrackStation |

---

## 🧩 Description

A challenge accessed via SSH that presented a username 
and a hash. The goal was to crack the hash — but each 
cracked result revealed another hash of a different type. 
This repeated across 5 layers until the final value 
revealed the flag.

---

## 🔍 Initial Access

Connected to the challenge server via SSH using 
the provided credentials:
```bash
ssh <username>@<host> -p <port>
```

The server greeted with a username and the 
first hash to crack.

---

## ⚔️ Attack Process

### Layer 1
- Received a hash string
- Used **hash-identifier** to identify the hash type
- Cracked it using CrackStation / John the Ripper
- Result was not the flag — it was another hash

### Layer 2
- New hash, different type than Layer 1
- Identified hash type again
- Cracked successfully
- Result was again another hash

### Layer 3
- Same process — different hash type
- Cracked successfully
- Another hash returned

### Layer 4
- Different hash type again
- Cracked successfully
- Another hash returned

### Layer 5 — Final Layer
- Cracked the final hash
- Submitted the result back to the SSH session
- Server accepted it and returned the flag
- SSH session closed automatically after flag was revealed

---

## 🚩 Flag
```
[flag captured]
```

---

## 💡 Lessons Learned

- Hashes have different types — MD5, SHA1, SHA256, 
  bcrypt etc — always identify before cracking
- **hash-identifier** is your first tool when you 
  see an unknown hash
- CrackStation is great for quick online cracking 
  of common hashes
- John the Ripper handles offline cracking with 
  wordlists like rockyou.txt
- Challenges can chain multiple layers — don't 
  assume first crack = done
- Automating repetitive tasks with a script 
  saves a lot of time

---

## 🛠️ Tools Used

- **SSH** — Remote server access
- **hash-identifier** — Identifying hash types
- **CrackStation** — Online hash cracking
- **John the Ripper** — Offline hash cracking
- **Kali Linux** — Testing environment

---

*Solved as part of PicoCTF practice — legal 
controlled environment*
