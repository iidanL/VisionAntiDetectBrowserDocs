# Export Cookies

Export all cookies from a specific browser profile.

## Endpoint

```
GET https://api.browser.vision/api/profiles/{profile_id}/cookies/export
```

## Headers

```
X-Token: your_token_here
```

## Python Example

```python
import requests

profile_id = "your_profile_id"
url = f"https://api.browser.vision/api/profiles/{profile_id}/cookies/export"
headers = {"X-Token": "your_token_here"}
response = requests.get(url, headers=headers)
cookies = response.json()
print(cookies)
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

> ℹ️ Exported cookies can be reused for login restoration or state replication across sessions.