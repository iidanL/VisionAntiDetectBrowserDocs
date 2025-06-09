# Create Folder

Create a new folder in your account or team.

## Endpoint

```
POST https://api.browser.vision/api/folders
Content-Type: application/json
```

## Headers

```
X-Token: your_token_here
```

## Request Body

```json
{
  "name": "New Folder",
  "team_id": "optional-team-id"
}
```

## Response

```json
{
  "id": "new-folder-id",
  "name": "New Folder",
  "profiles_count": 0
}
```