# drafts
Design documentation of Neutralinojs

# Roadmap/Plan

- Refactoring macOS version for v2 using core-shared APIs.
- Doing improvements to the window customization (via `neutralino.config.json`).
  * `minHeight`, `minWidth`, `maxWidth`, `maxHeight`, `resizable`, and `maximizable`.
  * Transparency level setting `opacity: number`.
- `enableServer: boolean` and `enableNativeAPI: boolean` Useful when setting a remote URL for the entry URL property.
- New methods to the native API.
  * `async filesystem.readBinaryFile` and `async filesystem.writeBinaryFile`
  * Tray menu API `async os.setTrayMenu()`. 
  * `Neutralino.events`. Centralized namesapce for native events. Eg: `Neutralino.events.onWindowMove`
