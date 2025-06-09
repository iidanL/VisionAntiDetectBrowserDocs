# Get Status List

Retrieve all custom statuses available in your account or team.

## Endpoint

```
GET https://api.browser.vision/api/statuses
```

## Headers

```
X-Token: your_token_here
```

## Python Example

```python
import requests

headers = {"X-Token": "your_token_here"}
response = requests.get("https://api.browser.vision/api/statuses", headers=headers)
print(response.json())
```

## Response Example

```json
[
  {
    "id": "status-id",
    "name": "Pending",
    "color": "#FFA500"
  }
]
```