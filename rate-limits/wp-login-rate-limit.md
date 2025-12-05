# Rate Limit wp-login.php

**Category:** Rate Limiting  
**Purpose:** Prevent rapid login attempts from a single IP.

## Rule Expression

```cf-expression
(http.request.uri.path eq "/wp-login.php")
```

## Suggested Action

- Action: Managed Challenge
- Threshold: 10 requests per 1 minute
- Penalty TTL: 600 seconds

## Notes

Combining this with a firewall rule provides both proactive and reactive protection.
