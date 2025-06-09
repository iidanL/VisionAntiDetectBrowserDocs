# NOT OFFICIAL Browser Vision API Documentation

This repository contains structured documentation for the [Browser Vision](https://browser.vision) API, designed for automating and managing browser profiles via HTTP API and DevTools Protocol.

## Documentation Structure

Documentation is organized into categories using separate Markdown files:

```
📁 browser-vision-api-docs/
├── README.md
├── 01_about/
│   ├── about-api.md
│   ├── auth.md
│   ├── start-stop.md
│   └── base-automation.md
├── 02_folders/
│   ├── general.md
│   ├── get-folder-list.md
│   ├── create-folder.md
│   ├── edit-folder.md
│   └── delete-folder.md
├── 03_profiles/
│   ├── general.md
│   ├── get-profiles-list.md
│   ├── get-profile-info.md
│   ├── get-new-fingerprint.md
│   ├── import-cookies.md
│   ├── export-cookies.md
│   ├── create-profile.md
│   ├── edit-profile.md
│   └── delete-profile.md
├── 04_proxy/
│   ├── general.md
│   ├── get-proxy-list.md
│   ├── create-proxy.md
│   ├── edit-proxy.md
│   └── delete-proxy.md
├── 05_statuses/
│   ├── general.md
│   ├── get-status-list.md
│   ├── create-status.md
│   ├── edit-status.md
│   └── delete-status.md
└── 06_tags/
    ├── general.md
    ├── get-tag-list.md
    ├── create-tag.md
    ├── edit-tag.md
    └── delete-tag.md
```

Each file contains a brief method description, request and response structure, and usage examples (mainly in JavaScript and Python).

## Usage Examples

The API supports standard HTTP methods: `GET`, `POST`, `PATCH`, `DELETE`. Authentication is handled via the `X-Token` header. Some requests in team mode also require `X-Team-Token`.

Browser integration is possible using:

* Puppeteer (Node.js)
* Playwright (Node.js, Python, C#)
* chromedp (Go)
* Chromiumoxide (Rust)

## Notes

All examples use the test host `http://127.0.0.1:3030`. It is recommended to replace it with your production host IP during deployment.

## Attribution and License

This documentation is based on the official pages from [docs.browser.vision](https://docs.browser.vision) and formatted into markdown files for easier local usage and CI/CD integration.
