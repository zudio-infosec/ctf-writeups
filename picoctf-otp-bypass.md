# 🔐 PicoCTF — OTP Bypass

## Challenge Info

| Field | Details |
|---|---|
| Platform | PicoCTF |
| Category | Web Exploitation |
| Difficulty | Easy |
| Tools Used | Burp Suite, Kali Linux |

---

## 🧩 Description

A web application with a registration flow that requires 
OTP verification before completing signup. The goal was 
to bypass the OTP step and complete registration without 
a valid OTP code.

---

## 🔍 Reconnaissance

Visiting the target page revealed a registration form 
with the following fields:

- First Name
- Last Name
- Phone Number
- Email Address
- Address

After submitting the form, the application redirected 
to an OTP verification page requiring a valid code 
before the account could be created.

---

## ⚔️ Attack Process

**Step 1 — Set up Burp Suite Interceptor**

Opened Burp Suite and enabled the Intercept under 
the Proxy tab to capture outgoing HTTP requests.

**Step 2 — Submit the Registration Form**

Filled in the registration form with test data and 
clicked submit. Burp Suite intercepted the POST 
request before it reached the server.

**Step 3 — Forward to Repeater**

Sent the intercepted request to the Repeater tab 
(Ctrl+R) to allow manual manipulation and repeated 
testing of the request.

**Step 4 — Manipulate the Request**

Analyzed the request parameters in Repeater. 
Manipulated the OTP-related parameter in the 
request to bypass the verification check.

**Step 5 — OTP Bypassed**

After manipulating the request and resending it, 
the server accepted it and the OTP verification 
was successfully bypassed.

---

## 🚩 Flag
```
[flag captured]
```

---

## 💡 Lessons Learned

- Never trust client-side validation alone
- OTP verification must be enforced strictly 
  on the server side
- Burp Suite Repeater is a powerful tool for 
  manually testing and manipulating HTTP requests
- Always intercept and analyze requests before 
  they reach the server during web app testing

---

## 🛠️ Tools Used

- **Burp Suite** — HTTP interception and request manipulation
- **Kali Linux** — Testing environment

---

*Solved as part of PicoCTF practice — legal 
controlled environment*
