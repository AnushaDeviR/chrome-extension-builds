# Basics

1. Basic manifest file must contain the following:

```js
{
  "manifest_version": 3,
  "name": "Hello Extensions",
  "description": "Base Level Extension",
  "version": "1.0",
  "action": {
    "default_popup": "hello.html",
    "default_icon": "hello_extensions.png"
  }
}
```

    - where `action` contain the html page and logo used for the extension

2. Usually the extension directory is loaded onto the extensions page with the developer mode on via the `Load unpacked` button.

3. Once the extension directory is loaded, we could use it by reloading the package whenever there's an update -> although this would only work for projects with plain html, css and js where the directory is not built using npm or other frameworks

4. There's an npm package called `chrome-types` that comes handy for auto-completion

5. In order to debug the extension using developer tool, enable it by adding the `popup.js` onto the html script

6. Folder structure:

```
   |__ extension project
        |__ manifest.json (config file containing all the metadata for the extension)
        |__ background.js (script that runs on the background)
        |__ scripts/
                |__ content.js (script that's injected into the web pages
                                that allows interaction with the web page)
        |__ popup/
            |__ popup.html (defines the structure of the popup/extension window)
            |__ popup.js (adds interactivity to the popup window)
            |__ popup.css (adds styling to the popup window)

        |__ images/
            |__ icon1.png (contains the logo or the icon files which is usually in 16x16 pixel)
```

## References:

- [Chrome documentation](https://developer.chrome.com/docs/extensions/get-started/tutorial/hello-world)
