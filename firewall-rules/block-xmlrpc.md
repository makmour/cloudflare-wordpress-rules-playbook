# Block XML-RPC Access

**Category:** Firewall Rule  
**Purpose:** Prevent brute force and DDoS attacks targeting `xmlrpc.php`.

## Rule Expression

```cf-expression
(http.request.uri.path contains "/xmlrpc.php")
```

## Suggested Action

- Action: Block

## Notes

Unless you're using services that depend on XML-RPC (e.g. Jetpack, remote publishing), it's safe to block this endpoint.
