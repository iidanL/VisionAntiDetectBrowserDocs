# Tags: General Overview

Tags in Browser Vision are user-defined labels used to categorize and filter browser profiles across folders or teams.

## Key Capabilities

* Assign multiple tags to profiles
* Filter profiles by tags in the UI and API
* Edit or remove tags as needed

## Authentication

All tag-related endpoints require:

```
X-Token: your_token_here
```

## Python Example (fetching all tags)

```python
import requests

headers = {"X-Token": "your_token_here"}
response = requests.get("https://api.browser.vision/api/tags", headers=headers)
print(response.json())
```