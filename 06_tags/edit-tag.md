# Edit Tag

Update an existing tag's name or color.

## Endpoint

```
PATCH https://api.browser.vision/api/tags/{tag_id}
Content-Type: application/json
```

## Headers

```
X-Token: your_token_here
```

## Request Body

```json
{
  "name": "revised-tag",
  "color": "#FF4500"
}
```

## Python Example

```python
import requests

tag_id = "your_tag_id"
url = f"https://api.browser.vision/api/tags/{tag_id}"
data = {
    "name": "revised-tag",
    "color": "#FF4500"
}
headers = {"X-Token": "your_token_here"}
response = requests.patch(url, json=data, headers=headers)
print(response.json())
```

## Response

```json
{
  "id": "tag_id",
  "name": "revised-tag",
  "color": "#FF4500"
}
```