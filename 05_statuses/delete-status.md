# Delete Status

Remove a custom status.

## Endpoint

```
DELETE https://api.browser.vision/api/statuses/{status_id}
```

## Headers

```
X-Token: your_token_here
```

## Python Example

```python
import requests

status_id = "your_status_id"
url = f"https://api.browser.vision/api/statuses/{status_id}"
headers = {"X-Token": "your_token_here"}
response = requests.delete(url, headers=headers)
print(response.json())
```

## Response

```json
{
  "success": true,
  "deleted": "status_id"
}
```