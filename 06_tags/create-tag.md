# Create Tag

Create a new tag to organize browser profiles.

## Endpoint

```
POST https://api.browser.vision/api/tags
Content-Type: application/json
```

## Headers

```
X-Token: your_token_here
```

## Request Body

```json
{
  "name": "automation",
  "color": "#FFD700"
}
```

## Python Example

```python
import requests

headers = {"X-Token": "your_token_here"}
data = {
    "name": "automation",
    "color": "#FFD700"
}
response = requests.post("https://api.browser.vision/api/tags", json=data, headers=headers)
print(response.json())
```

## Response

```json
{
  "id": "new-tag-id",
  "name": "automation",
  "color": "#FFD700"
}
```