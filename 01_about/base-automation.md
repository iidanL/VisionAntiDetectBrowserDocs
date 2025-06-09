# Base Automation

To automate browser behavior inside a running profile, you can connect to the instance using DevTools Protocol through tools like Pyppeteer, Playwright (Python), and others.

## Prerequisite

The profile must be started via the `/start/{folderId}/{profileId}` endpoint with a remote debugging port set in the `args`.

## Pyppeteer Example (Python)

```python
import asyncio
from pyppeteer import connect

async def main():
    browser = await connect(browserURL='http://127.0.0.1:9222')
    page = await browser.newPage()
    await page.goto('https://example.com')
    await browser.disconnect()

asyncio.get_event_loop().run_until_complete(main())
```

## Playwright Example (Python)

```python
from playwright.sync_api import sync_playwright

with sync_playwright() as p:
    browser = p.chromium.connect_over_cdp('http://127.0.0.1:9222')
    context = browser.contexts[0]
    page = context.new_page()
    page.goto('https://example.com')
    browser.close()
```

## Other Supported Clients

* **Playwright (C#)**
* **chromedp (Go)**
* **Chromiumoxide (Rust)**