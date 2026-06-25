# 🔐 PicoCTF — WebDecode

## Challenge Info

| Field | Details |
|---|---|
| Platform | PicoCTF |
| Category | Web Exploitation |
| Difficulty | Easy |
| URL | http://titan.picoctf.net:61645/ |
| Tools Used | Browser DevTools, base64 |

---

## 🧩 Description

A website with three pages — Home, About Us, 
and Contact. The goal was to find and decode 
a hidden flag somewhere on the site.

---

## 🔍 Reconnaissance

Visited all three pages of the website. Nothing 
obvious on the surface. 

Opened **View Page Source** on the About Us page 
and carefully read through the HTML.

---

## 🔎 Finding The Flag

Inside the page source found a suspicious HTML 
attribute that is not a standard HTML attribute:
```html
<section class="about" notify_true="cGljb0NURnt3ZWJfc3VjYzNzc2Z1bGx5X2QzYzBkZWRfZGYwZGE3Mjd9">
```

The value of `notify_true` looked like a 
Base64 encoded string — identified by the 
character set and the `=` padding pattern 
common in Base64.

---

## ⚔️ Decoding

Decoded the string using terminal:
```bash
echo "cGljb0NURnt3ZWJfc3VjYzNzc2Z1bGx5X2QzYzBkZWRfZGYwZGE3Mjd9" | base64 -d
```

---

## 🚩 Flag
```
picoCTF{web_succ3ssfully_d3c0ded_df0da727}
```

---

## 💡 Lessons Learned

- Always check page source — not just what 
  you see visually in the browser
- Developers sometimes hide data in custom 
  HTML attributes
- Base64 strings are recognizable by their 
  character pattern — letters, numbers, 
  `+`, `/` and `=` padding at the end
- `base64 -d` in terminal is the fastest 
  way to decode on Kali Linux
- Every page of a website is worth inspecting,
  not just the main page

---

## 🛠️ Tools Used

- **Browser** — View Page Source
- **Terminal** — `base64 -d` command
- **Kali Linux** — Testing environment

---

*Solved as part of PicoCTF practice — legal 
controlled environment*
