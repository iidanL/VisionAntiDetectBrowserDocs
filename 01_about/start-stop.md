# Start/Stop Browser Profiles

The Browser Vision API allows programmatic control over starting and stopping browser profiles via local HTTP endpoints.

## Start a Profile

### GET Request

```
GET http://127.0.0.1:3030/start/{folderId}/{profileId}
```

### POST Request (with options)

```
POST http://127.0.0.1:3030/start/{folderId}/{profileId}
Content-Type: application/json
```

**Example body:**

```json
{
  "args": ["--headless"]
}
```

## Stop a Profile

```
GET http://127.0.0.1:3030/stop/{folderId}/{profileId}
```

Or use a POST request without a body.

## List Running Profiles

```
GET http://127.0.0.1:3030/list
```

## Python Example: List Running Profiles

```python
import requests

headers = {"X-Token": "your_token_here"}
response = requests.get("http://127.0.0.1:3030/list", headers=headers)
print(response.json())
```

## Response Example

```json
{
  "profiles": [
    {
      "folder_id": "uuid-folder",
      "profile_id": "uuid-profile",
      "port": 9222
    }
  ]
}
```

> ℹ️ Profiles must be started with a remote debugging port to enable automation tools like Playwright.