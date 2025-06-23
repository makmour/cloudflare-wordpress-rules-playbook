# Static Endpoint Bot Rate Limit

**Category:** Rate Limiting  
**Type:** Expression Builder Compatible  
**Purpose:** Protect against bot abuse of static endpoints like favicon, robots.txt, and feeds.

## 🔐 Rule Expression

```cf-expression
(http.request.uri.path contains "/favicon.ico") or
(http.request.uri.path contains "/robots.txt") or
(http.request.uri.path contains ".xml") or
(http.request.uri.path contains ".rss") or
(http.request.uri.path contains ".atom")
```

## ✅ Suggested Action

- Action: Managed Challenge
- Threshold: 15 requests/min per IP
- Period: 60 seconds
- Penalty TTL: 600 seconds

## 📌 Notes

This rule helps mitigate low-level DoS attacks and unnecessary load by rate limiting redundant bot traffic.
