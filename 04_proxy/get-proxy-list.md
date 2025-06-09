# Get Proxy List

Retrieve a list of proxies associated with the current account or team.

## Endpoint

```
GET https://api.browser.vision/api/proxy
```

## Headers

```
X-Token: your_token_here
```

## Python Example

```python
import requests

headers = {"X-Token": "your_token_here"}
response = requests.get("https://api.browser.vision/api/proxy", headers=headers)
print(response.json())
```

## Response Example

```json
[
  {
    "id": "proxy-id",
    "host": "123.456.789.0",
    "port": 8080,
    "type": "http",
    "status": "active"
  }
]
```