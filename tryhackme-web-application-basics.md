# Web Application Basics - TryHackMe Writeup

**Room:** Web Application Basics  
**Difficulty:** Easy  
**Category:** Web Security  
**Date Completed:** 2025  
**Platform:** TryHackMe

## Challenge Description
Learn the basics of web applications: HTTP, URLs, request methods, response codes, and headers.

## HTTP Protocol

### Request Methods
| Method | Description |
|--------|-------------|
| GET | Retrieve data |
| POST | Submit data |
| PUT | Update data |
| DELETE | Remove data |
| PATCH | Partial update |

### Common Headers

**Request Headers:**
- `Host` - Target domain
- `User-Agent` - Client browser
- `Accept` - Expected response type
- `Cookie` - Session data
- `Authorization` - Credentials

**Response Headers:**
- `Server` - Web server info
- `Set-Cookie` - Set session cookie
- `Content-Type` - Response format
- `Content-Length` - Response size

### Status Codes

**1xx - Informational**
- 100 Continue
- 101 Switching Protocols

**2xx - Success**
- 200 OK
- 201 Created
- 204 No Content

**3xx - Redirection**
- 301 Moved Permanently
- 302 Found
- 304 Not Modified

**4xx - Client Error**
- 400 Bad Request
- 401 Unauthorized
- 403 Forbidden
- 404 Not Found

**5xx - Server Error**
- 500 Internal Server Error
- 502 Bad Gateway
- 503 Service Unavailable

## URL Structure
```
scheme://username:password@domain:port/path?query#fragment
```

Example:
```
https://example.com:443/path/to/page?id=123#section
```

## Key Concepts

### Sessions & Cookies
- Server creates session
- Session ID sent in cookie
- Client stores cookie
- Each request includes cookie

### HTTPS/TLS
- Encrypts traffic
- Certificate verification
- Prevents MITM attacks

## Learning Points
- HTTP is stateless
- Headers contain metadata
- Status codes indicate result

---
*Writeup by @zudio-infosec*  
*For more: github.com/zudio-infosec/ctf-writeups*