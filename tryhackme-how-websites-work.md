# How Websites Work - TryHackMe Writeup

**Room:** How Websites Work  
**Difficulty:** Easy  
**Category:** Web Basics  
**Date Completed:** 2025  
**Platform:** TryHackMe

## Challenge Description
To exploit a website, you first need to know how they are created.

## How Websites Work

### Frontend (Client-Side)
- **HTML** - Structure
- **CSS** - Styling
- **JavaScript** - Interactivity

### Backend (Server-Side)
- **Server** - Processes requests
- **Database** - Stores data
- **Application** - Business logic

## HTTP Protocol

### Request Methods
- **GET** - Retrieve data
- **POST** - Send data
- **PUT** - Update data
- **DELETE** - Remove data

### Status Codes
- 200 OK - Success
- 301 Redirect - Permanent move
- 302 Redirect - Temporary move
- 400 Bad Request - Client error
- 401 Unauthorized - Auth required
- 403 Forbidden - Access denied
- 404 Not Found - Resource missing
- 500 Server Error - Server problem

### HTTP Headers
- User-Agent
- Cookie
- Authorization
- Content-Type
- Host

## Request/Response Cycle
1. Client sends HTTP request
2. Server processes request
3. Server queries database (if needed)
4. Server generates response
5. Response sent to client

## Key Components
- **URL** - Uniform Resource Locator
- **DNS** - Domain Name System
- **Cookies** - State management
- **Sessions** - Server-side state

## Learning Points
- Understanding web architecture is crucial
- Both frontend and backend matter for security
- HTTP is the foundation of web communication

---
*Writeup by @zudio-infosec*  
*For more: github.com/zudio-infosec/ctf-writeups*