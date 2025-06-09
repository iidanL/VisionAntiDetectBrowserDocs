# Get Folder List

Retrieves all folders accessible by the user.

## Endpoint

```
GET https://api.browser.vision/api/folders
```

## Headers

```
X-Token: your_token_here
```

## Response Example

```json
[
  {
    "id": "folder-uuid",
    "name": "Marketing",
    "team_id": "team-uuid",
    "profiles_count": 12
  }
]
```