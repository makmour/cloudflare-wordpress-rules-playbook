# Protect wp-admin Directory

**Category:** Firewall Rule  
**Purpose:** Block or challenge bots scanning admin endpoints.

## 🔐 Rule Expression

```cf-expression
http.request.uri.path contains "/wp-admin"
```

## ✅ Suggested Action

- Action: Managed Challenge

## 📌 Notes

Avoid applying strict cache rules here. Protect access without blocking legitimate users.
