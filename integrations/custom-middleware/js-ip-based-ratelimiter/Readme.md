## Getting Started
1. Set the `APIID` and `ORGID` values inside `integrations/custom-middleware/js-ip-based-ratelimiter/src/middleware/ipRateLimiter.js`.

2. Add the following to your API definition:

```
"custom_middleware": {
  "pre": [
    {
      "name": "ipRateLimiter",
      "path": "/etc/middleware/ipRateLimiter.js",
      "require_session": false,
      "raw_body_only": false
    }
  ],
```

3. Make sure `Authentication mode` is set to `Authentication Token` and `Auth Key Header Name` is set to `Authorization` in your API.

4. Add `X-Real-Ip` as a header to your request. Sample request: `curl localhost:8080/hello-tyk/get -H "X-Real-Ip:127.0.0.1"`