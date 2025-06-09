# Delete Profile

Delete a specific browser profile.

## Endpoint

```
DELETE https://api.browser.vision/api/profiles/{profile_id}
```

## Headers

```
X-Token: your_token_here
```

## Response

```json
{
  "success": true,
  "deleted": "profile_id"
}
```

> ⚠️ This operation is irreversible.