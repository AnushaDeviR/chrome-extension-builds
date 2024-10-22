# Read Time Extension

- The following project has been used as a study material here from Google's Chrome Extension Documentation

# Learning Notes:

## About the manifest.json file:

- The `manifest.json` file must always be on the root directory.
- The required keys on the manifest are: `manifest_version`, `name`, `version`
- For commenting on the manifest file: `//` can be used but must be deleted before uploading it to the extension store
- Icons are recommended to be in `png` with the following sizes: 16x16, 32x32, 48x48, 128x128
  - 16x16: favicon on extension's page and context menu
  - 32x32: on windows computer
  - 48x48: on Extension page
  - 128x128: on Chrome Web Store during installation

## Content script:

- To read and modify the content of the page, content.js is used.
- They are in isolation and won't conflict with the host's JS or other extension's content scripts

```json
// on manifest.json
{
  "content_scripts": [
    {
      "js": ["scripts/content.js"],
      //   allows the browser to identify the sites to inject in (matches: <scheme>://<host><path>)
      "matches": [
        "https://developer.chrome.com/docs/extensions/*",
        "https://developer.chrome.com/docs/webstore/*"
      ]
    }
  ]
}
```
