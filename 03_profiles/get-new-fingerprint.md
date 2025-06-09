# Get New Fingerprint

Generate a new fingerprint configuration to use when creating or updating a profile.

## Endpoint

```
GET https://api.browser.vision/api/profiles/fingerprint
```

## Headers

```
X-Token: your_token_here
```

## Python Example

```python
import requests

headers = {"X-Token": "your_token_here"}
response = requests.get("https://api.browser.vision/api/profiles/fingerprint", headers=headers)
print(response.json())
```

## Response Example

```json
{
  "fingerprint": {
    "userAgent": "Mozilla/5.0...",
    "platform": "Win32",
    "language": "en-US",
    "timezone": "America/New_York"
  }
}
```

> ℹ️ Use this fingerprint when creating or modifying a browser profile.