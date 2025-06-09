# Edit Profile

Update the settings or metadata of a browser profile.

## Endpoint

```
PATCH https://api.browser.vision/api/profiles/{profile_id}
Content-Type: application/json
```

## Headers

```
X-Token: your_token_here
```

## Request Body Example

```json
{
  "name": "Updated Name",
  "tags": ["new-tag"]
}
```

## Response

```json
{
  "id": "profile_id",
  "name": "Updated Name"
}
```