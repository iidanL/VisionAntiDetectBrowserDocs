# Edit Proxy

Update the configuration of an existing proxy.

## Endpoint

```
PATCH https://api.browser.vision/api/proxy/{proxy_id}
Content-Type: application/json
```

## Headers

```
X-Token: your_token_here
```

## Request Body Example

```json
{
  "host": "123.456.789.1",
  "port": 3128,
  "type": "socks5",
  "login": "newuser",
  "password": "newpass"
}
```

## Python Example

```python
import requests

proxy_id = "your_proxy_id"
url = f"https://api.browser.vision/api/proxy/{proxy_id}"
headers = {"X-Token": "your_token_here"}
data = {
    "host": "123.456.789.1",
    "port": 3128,
    "type": "socks5",
    "login": "newuser",
    "password": "newpass"
}
response = requests.patch(url, json=data, headers=headers)
print(response.json())
```

## Response

```json
{
  "success": true,
  "updated": "proxy_id"
}
```