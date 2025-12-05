# Cache Everything on Homepage

**Category:** Cache Rule  
**Purpose:** Improve performance and reduce origin load for anonymous traffic.

## Rule Expression

```cf-expression
(http.request.uri.path eq "/")
```

## Suggested Action

- Action: Cache Everything
- Edge TTL: 1 hour or longer
- Browser TTL: Respect existing headers

## Notes

Avoid applying this rule to logged-in users. Pair with a bypass rule for wp-admin, cart, checkout, etc.
