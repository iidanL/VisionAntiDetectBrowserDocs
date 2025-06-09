# About the API (Updated)

The Browser Vision API allows developers to automate both internal operations (such as profile, folder, and proxy management) and external browser behavior using DevTools Protocols like Puppeteer and Playwright.

## Capabilities

* Manage browser profiles, folders, proxies, tags, and statuses.
* Start and stop profiles programmatically.
* Control browser sessions with Puppeteer, Playwright, etc.

## Two Levels of Automation

### 1. Application-Level API

Use HTTP requests (GET, POST, PATCH, DELETE) with the required headers to manage resources such as:

* Profiles
* Folders
* Proxies
* Tags
* Statuses

**Authentication:**

* `X-Token` – required for all API requests.
* `X-Team-Token` – used when team mode is enabled.

### 2. Profile-Level Automation

Use tools like Puppeteer, Playwright, or Selenium to connect to running browser profiles via DevTools Protocol. These profiles must be launched using the start API beforehand.

## Python Example: Fetch Folders

```python
import requests

headers = {"X-Token": "your_token_here"}
response = requests.get("https://api.browser.vision/api/folders", headers=headers)
print(response.json())
```