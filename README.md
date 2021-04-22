# drafts
Design documentation of Neutralinojs

# Roadmap/Plan

- Refactoring macOS version for v2 using core-shared APIs.
- Doing improvements to the window customization (via `neutralino.config.json`).
  * `minHeight`, `minWidth`, `maxWidth`, `maxHeight`, `resizable`, and `maximizable`.
  * Transparency level setting `opacity: number`.
  * `hidden: boolean` - A nice way to write background apps.
- `enableHTTPServer: boolean` and `enableNativeAPI: boolean` Useful when setting a remote URL for the entry URL property. **Added**
- Adding new methods to the native API.
  * `async filesystem.readBinaryFile` and `async filesystem.writeBinaryFile`
  * GUI manipulation methods. Eg: `async app.maximize()`
  * Tray menu API `async os.setTrayMenu()`. 
  * `Neutralino.events`. Centralized namesapce for native events. Eg: `Neutralino.events.onWindowMove`
