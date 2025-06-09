# Profiles: General Overview

Browser profiles in Browser Vision provide isolated environments with separate cookies, cache, storage, and proxy configurations. They are essential for managing automated workflows and multiple identities.

## Key Capabilities

* Create and delete profiles
* Retrieve profile data and settings
* Edit configurations, assign tags or statuses
* Import/export cookies

## Authentication

All profile-related API requests require:

```
X-Token: your_token_here
```

## Python Example: Fetch Profiles in a Folder

```python
import requests

folder_id = "your_folder_id"
url = f"https://api.browser.vision/api/folders/{folder_id}/profiles"
headers = {"X-Token": "your_token_here"}
response = requests.get(url, headers=headers)
print(response.json())
```