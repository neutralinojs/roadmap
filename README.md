# drafts
Feature proposals of Neutralinojs

# Roadmap/Plan

- Refactoring macOS version for v2 using core-shared APIs. **(Blocker)**
- Doing improvements to the window customization (via `neutralino.config.json`).
  * `minHeight`, `minWidth`, `maxWidth`, `maxHeight`, `resizable`, and `maximizable`.
  * Transparency level setting `opacity: number`.
  * `hidden: boolean` - A nice way to write background apps. **(Added)**
- `enableHTTPServer: boolean` and `enableNativeAPI: boolean` Useful when setting a remote URL for the entry URL property. **(Added)**
- Adding new methods to the native API.
  * `async filesystem.readBinaryFile` and `async filesystem.writeBinaryFile`
  * GUI manipulation methods. Eg: `async app.maximize()`
  * Tray menu API `async os.setTrayMenu()`. 
  * `Neutralino.events`. Centralized namesapce for native events. Eg: `Neutralino.events.onWindowMove`
- Neutralino API extensions - Developers can make their own backend code with Go. STDIN/STDOUT is used as the communication channel.
```js
Neutralino.app.sendExtMessage(ExtensionMessageOptions)
/*
*   ExtensionMessageOptions
*   {
*    extension: "myExtension" // binaryName
*    data: {} //json Message
*   }
*
*  ./extensions/bin/myExtension-win
*  ./extensions/bin/myExtension-linux
*  ./extensions/bin/myExtension-mac
*
*  ./extensions/src/myExtension.go
*   
*  "neu extensions --build" - Make binaries for all extensions
*  "neu extensions" - Lists existing extensions
*
*/
```
