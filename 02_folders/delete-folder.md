# Delete Folder

Remove a folder and all associated data.

## Endpoint

```
DELETE https://api.browser.vision/api/folders/{folder_id}
```

## Headers

```
X-Token: your_token_here
```

## Response

```json
{
  "success": true,
  "deleted": "folder_id"
}
```

> ⚠️ Deleting a folder also deletes its associated profiles.