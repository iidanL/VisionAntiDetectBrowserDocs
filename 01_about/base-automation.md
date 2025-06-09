# Base Automation (Updated)

To automate browser behavior inside a running profile, connect to the instance using DevTools Protocol through libraries such as Pyppeteer or Playwright for Python.

## Prerequisite

The profile must be started via the `/start/{folderId}/{profileId}` endpoint with a remote debugging port set in the `args`.

## Python Example: Pyppeteer

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

## Python Example: Playwright

```python
from playwright.sync_api import sync_playwright

with sync_playwright() as p:
    browser = p.chromium.connect_over_cdp('http://127.0.0.1:9222')
    context = browser.contexts[0]
    page = context.new_page()
    page.goto('https://example.com')
    browser.close()
```

> 💡 Be sure to launch the profile with the appropriate port using the start API to enable CDP-based control.