# Get New Fingerprint

Generate a new fingerprint configuration for a profile.

## Endpoint

```
GET https://api.browser.vision/api/profiles/fingerprint
```

## Headers

```
X-Token: your_token_here
```

## Response Example

```json
{
  "fingerprint": {
    "userAgent": "...",
    "platform": "...",
    "language": "...",
    "timezone": "...",
    ...
  }
}
```