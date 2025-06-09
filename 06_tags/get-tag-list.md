# Get Tag List

Retrieve all tags available in your account.

## Endpoint

```
GET https://api.browser.vision/api/tags
```

## Headers

```
X-Token: your_token_here
```

## Python Example

```python
import requests

headers = {"X-Token": "your_token_here"}
response = requests.get("https://api.browser.vision/api/tags", headers=headers)
print(response.json())
```

## Response Example

```json
[
  {
    "id": "tag-id",
    "name": "automation",
    "color": "#FFD700"
  }
]
```