# Authentication

To use the Browser Vision API, all HTTP requests must include authentication tokens in the request headers.

## Required Tokens

### `X-Token`

The primary token for authorizing requests. You can generate this token from the Vision application’s settings page.

### `X-Team-Token`

Used when team collaboration mode is enabled. This token grants access to shared resources within the team environment.

## Example Header

```http
X-Token: your_token_here
X-Team-Token: your_team_token_here  # only when required
```

## Usage

Tokens should be included with every API call, regardless of the endpoint. Unauthorized requests will be rejected with an HTTP 401 error.

> Note: Keep your tokens secure and do not share them publicly.