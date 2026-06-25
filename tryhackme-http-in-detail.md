# 🌐 TryHackMe — HTTP in Detail

## Room Info

| Field | Details |
|---|---|
| Platform | TryHackMe |
| Room | HTTP in Detail |
| Category | Web Fundamentals |
| Difficulty | Easy |
| Badge Earned | 🕸️ Webbed |

---

## 🧩 Description

A detailed room covering how HTTP works —
the foundation of all web communication.
Covers request/response structure, headers,
cookies, and status codes.

---

## 📚 Key Concepts Learned

### HTTP Request Types

| Method | Purpose |
|---|---|
| `GET` | Retrieve data from server |
| `POST` | Send data to server |
| `PUT` | Update existing data |
| `DELETE` | Delete data |

---

### Request Headers

Sent by the client to the server:

| Header | Purpose |
|---|---|
| `Host` | Which website you want |
| `User-Agent` | Your browser/client info |
| `Content-Type` | Type of data being sent |
| `Authorization` | Authentication credentials |
| `Cookie` | Stored session data |

---

### Response Headers

Sent by the server back to the client:

| Header | Purpose |
|---|---|
| `Content-Type` | Type of data being returned |
| `Set-Cookie` | Tells browser to store a cookie |
| `Cache-Control` | How long to cache the response |
| `Location` | Redirect destination |

---

### Status Codes

| Code | Meaning |
|---|---|
| `200` | OK — success |
| `201` | Created — resource created |
| `301` | Moved Permanently — redirect |
| `302` | Found — temporary redirect |
| `400` | Bad Request |
| `401` | Unauthorized |
| `403` | Forbidden — no permission |
| `404` | Not Found |
| `500` | Internal Server Error |
| `503` | Service Unavailable |

---

### Cookies

- Small pieces of data stored in your browser
- Set by server using `Set-Cookie` header
- Sent automatically with every request
- Used for session management and authentication
- Critical in security — stealing cookies = 
  stealing sessions
```
Server → Set-Cookie: session=abc123
Browser → stores it
Next request → Cookie: session=abc123
Server → recognizes you
```

---

### HTTP Request Structure
```
GET /page HTTP/1.1
Host: example.com
User-Agent: Mozilla/5.0
Cookie: session=abc123
```

### HTTP Response Structure
```
HTTP/1.1 200 OK
Content-Type: text/html
Set-Cookie: session=xyz789

<html>page content</html>
```

---

## 💡 Lessons Learned

- HTTP is the foundation of all web communication
- Every web request has headers carrying
  important metadata
- Cookies are critical for session management
  and are a major target for attackers
- Status codes tell you exactly what happened
  with a request
- Understanding HTTP deeply is essential
  for web application penetration testing

---

## 🏆 Badge Earned

**🕸️ Webbed** — Understands how the world wide web works

---

*Completed on TryHackMe — legal controlled
environment*
