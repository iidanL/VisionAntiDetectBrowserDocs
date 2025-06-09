# Create Status

Add a new custom status to your environment.

## Endpoint

```
POST https://api.browser.vision/api/statuses
Content-Type: application/json
```

## Headers

```
X-Token: your_token_here
```

## Request Body

```json
{
  "name": "In Progress",
  "color": "#00BFFF"
}
```

## Python Example

```python
import requests

headers = {"X-Token": "your_token_here"}
data = {
    "name": "In Progress",
    "color": "#00BFFF"
}
response = requests.post("https://api.browser.vision/api/statuses", json=data, headers=headers)
print(response.json())
```

## Response

```json
{
  "id": "new-status-id",
  "name": "In Progress",
  "color": "#00BFFF"
}
```