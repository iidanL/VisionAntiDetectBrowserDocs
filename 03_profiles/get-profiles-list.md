# Get Profiles List

Returns all profiles under a specified folder.

## Endpoint

```
GET https://api.browser.vision/api/folders/{folder_id}/profiles
```

## Headers

```
X-Token: your_token_here
```

## Python Example

```python
import requests

folder_id = "your_folder_id"
url = f"https://api.browser.vision/api/folders/{folder_id}/profiles"
headers = {"X-Token": "your_token_here"}
response = requests.get(url, headers=headers)
print(response.json())
```

## Response Example

```json
[
  {
    "id": "profile-id",
    "name": "Profile 1",
    "status": "active",
    "browser": "chrome",
    "created_at": "2024-01-01T12:00:00Z"
  }
]
```