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

You may also specify a remote debugging port:

```json
{
  "args": ["--remote-debugging-port=9222"]
}
```

## Stop a Profile

You can stop a running profile with:

```
GET http://127.0.0.1:3030/stop/{folderId}/{profileId}
```

Or using a POST request without a body.

## List Running Profiles

```
GET http://127.0.0.1:3030/list
```

**Response example:**

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

## Authentication

All requests require the `X-Token` header:

```http
X-Token: your_token_here
```