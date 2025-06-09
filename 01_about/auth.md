# Authentication

To use the Browser Vision API, all HTTP requests must include authentication tokens in the request headers.

## Required Tokens

### `X-Token`

The primary token for authorizing requests. You can generate this token from the Vision application’s settings page.

### `X-Team-Token`

Used when team collaboration mode is enabled. This token grants access to shared resources within the team environment.

## Example Headers

```
X-Token: your_token_here
X-Team-Token: your_team_token_here  # only when required
```

## Python Example: Using Auth Headers

```python
import requests

headers = {
    "X-Token": "your_token_here",
    "X-Team-Token": "your_team_token_here"  # optional
}
response = requests.get("https://api.browser.vision/api/folders", headers=headers)
print(response.json())
```

## Usage

Tokens must be included with every API call, regardless of the endpoint. Unauthorized requests will be rejected with an HTTP 401 error.

> ⚠️ Keep your tokens secure. Do not expose them in public code repositories.