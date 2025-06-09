# Edit Folder

Update the name of an existing folder.

## Endpoint

```
PATCH https://api.browser.vision/api/folders/{folder_id}
Content-Type: application/json
```

## Headers

```
X-Token: your_token_here
```

## Request Body

```json
{
  "name": "Updated Folder Name"
}
```

## Response

```json
{
  "id": "folder_id",
  "name": "Updated Folder Name"
}
```