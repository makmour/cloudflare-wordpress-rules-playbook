# Protect wp-login.php with Challenge

**Category:** Firewall Rule  
**Purpose:** Prevent unauthorized login attempts and brute force abuse.

## 🔐 Rule Expression

```cf-expression
(http.request.uri.path eq "/wp-login.php")
```

## ✅ Suggested Action

- Action: Managed Challenge

## 📌 Notes

Optionally restrict by country, IP range, or allow only known admin IPs.
