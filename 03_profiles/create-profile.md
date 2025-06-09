# Create Profile

Create a new browser profile under a specified folder.

## Endpoint

```
POST https://api.browser.vision/api/profiles
Content-Type: application/json
```

## Headers

```
X-Token: your_token_here
```

## Request Body

```json
{
  "name": "Test Profile",
  "folder_id": "folder-uuid",
  "browser": "chrome",
  "fingerprint": { ... },
  "tags": ["automation"]
}
```

## Response

```json
{
  "id": "new-profile-id",
  "name": "Test Profile"
}
```