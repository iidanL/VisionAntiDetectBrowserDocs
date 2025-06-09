# Export Cookies

Export cookies stored in a profile.

## Endpoint

```
GET https://api.browser.vision/api/profiles/{profile_id}/cookies/export
```

## Headers

```
X-Token: your_token_here
```

## Response Example

```json
{
  "cookies": [
    {
      "domain": ".example.com",
      "name": "sessionid",
      "value": "abc123",
      "path": "/",
      "expires": 1728000000,
      "httpOnly": true,
      "secure": true
    }
  ]
}
```