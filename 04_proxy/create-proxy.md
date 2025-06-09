# Create Proxy

Add a new proxy to your Browser Vision account.

## Endpoint

```
POST https://api.browser.vision/api/proxies
Content-Type: application/json
```

## Headers

```
X-Token: your_token_here
```

## Request Body

```json
{
  "type": "http",
  "ip": "192.168.0.1",
  "port": 8080,
  "login": "user",
  "password": "pass"
}
```

## Python Example

```python
import requests

url = 'https://api.browser.vision/api/proxies'
headers = { 'X-Token': 'your_token_here' }
data = {
    "type": "http",
    "ip": "192.168.0.1",
    "port": 8080,
    "login": "user",
    "password": "pass"
}
response = requests.post(url, json=data, headers=headers)
print(response.json())
```

## Response

```json
{
  "id": "new-proxy-id",
  "type": "http",
  "ip": "192.168.0.1"
}
```