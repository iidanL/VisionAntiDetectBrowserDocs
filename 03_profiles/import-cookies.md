# Import Cookies

Import cookies into a browser profile to simulate authenticated sessions or load session state.

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

## Python Example

```python
import requests

profile_id = "your_profile_id"
url = f"https://api.browser.vision/api/profiles/{profile_id}/cookies/import"
headers = {"X-Token": "your_token_here"}
cookies = {
    "cookies": [
        {
            "domain": ".example.com",
            "name": "sessionid",
            "value": "abc123",
            "path": "/",
            "expires": 1728000000,
            "httpOnly": True,
            "secure": True
        }
    ]
}
response = requests.post(url, json=cookies, headers=headers)
print(response.json())
```

## Response

```json
{
  "success": true
}
```

> ℹ️ Use valid domain-matching cookies. Incorrect formats may silently fail.