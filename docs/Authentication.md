---
stoplight-id: qf2gbk6f7p5ya
---

# Authentication

Starwipe uses API keys* to authenticate requests. An active API key must be included in the request header for all API calls.

- You can view and manage your API keys in your [developer dashboard](https://developer.starwipe.com/dashboard).
- You can have up to 2 API keys active at a time.
- Keys cannot be shared with another account.
- Be sure to keep your API keys secure and never expose them publicly.

<!-- theme: warning -->
> \*API calls may be sent over HTTPS only. Requests sent over basic HTTP will fail and return a `401 - Unauthorized` error. Calls missing an API key will also return a `401` error.
