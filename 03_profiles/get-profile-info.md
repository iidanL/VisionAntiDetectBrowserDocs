# Get Profile Info

Retrieve detailed information about a specific browser profile.

## Endpoint

```
GET https://api.browser.vision/api/profiles/{profile_id}
```

## Headers

```
X-Token: your_token_here
```

## Response Example

```json
{
  "id": "profile-id",
  "name": "Test Profile",
  "browser": "chrome",
  "created_at": "2024-01-01T12:00:00Z",
  "tags": ["automation", "test"]
}
```