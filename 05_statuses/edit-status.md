# Edit Status

Update an existing status.

## Endpoint

```
PATCH https://api.browser.vision/api/statuses/{status_id}
Content-Type: application/json
```

## Headers

```
X-Token: your_token_here
```

## Request Body

```json
{
  "name": "Completed",
  "color": "#32CD32"
}
```

## Python Example

```python
import requests

status_id = "your_status_id"
url = f"https://api.browser.vision/api/statuses/{status_id}"
data = {
    "name": "Completed",
    "color": "#32CD32"
}
headers = {"X-Token": "your_token_here"}
response = requests.patch(url, json=data, headers=headers)
print(response.json())
```

## Response

```json
{
  "id": "status_id",
  "name": "Completed",
  "color": "#32CD32"
}
```