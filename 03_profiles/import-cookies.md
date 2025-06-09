# Import Cookies

Import cookies into a browser profile.

## Endpoint

```
POST https://api.browser.vision/api/profiles/{profile_id}/cookies/import
Content-Type: application/json
```

## Headers

```
X-Token: your_token_here
```

## Request Body

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

## Response

```json
{
  "success": true
}
```