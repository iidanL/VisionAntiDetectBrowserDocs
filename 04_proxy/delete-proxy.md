# Delete Proxy

Remove a proxy from your account.

## Endpoint

```
DELETE https://api.browser.vision/api/proxy/{proxy_id}
```

## Headers

```
X-Token: your_token_here
```

## Python Example

```python
import requests

proxy_id = "your_proxy_id"
url = f"https://api.browser.vision/api/proxy/{proxy_id}"
headers = {"X-Token": "your_token_here"}
response = requests.delete(url, headers=headers)
print(response.json())
```

## Response

```json
{
  "success": true,
  "deleted": "proxy_id"
}
```