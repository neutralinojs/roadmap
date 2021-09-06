The roadmap of Neutralinojs

# Roadmap 2021

- Refactoring macOS version for v2 using core-shared APIs.  **(Done)**.
- Set exit code for `app.exit()` from JavaScript API. **(Done)**
- Doing improvements to the window customization (via `neutralino.config.json`).
  * `minHeight`, `minWidth`, `maxWidth`, `maxHeight`, and `resizable` **(Done)**.
  * Transparency level setting `opacity: number`.
  * `hidden: boolean` - A nice way to write background apps. **(Done)**
- `enableHTTPServer: boolean` and `enableNativeAPI: boolean` Useful when setting a remote URL for the entry URL property. **(Done)**
- Implement a way to change the path context via command line. Keep Neutralino binaries without renaming inside the `bin` directory.  **(Done)**
- Adding new methods to the native API.
  * `async filesystem.readBinaryFile`, `async filesystem.writeBinaryFile`, `async filesystem.getStats` and `async filesystem.copyFile` - **(Done)**
  * GUI manipulation methods. Eg: `window.setTitle(string title)` etc. **(Done)**
  * Tray menu API `async os.setTrayMenu()`. **(Done)**
  * `Neutralino.events`. Centralized namesapce for native events. **(Done)**
- Neutralino API extensions - Developers can make their own backend code with any programming language (C++, Go, and Rust are recommended). STDIN/STDOUT is used as the communication channel.
```js
await Neutralino.app.sendExtMessage(ExtensionMessageOptions)
/*
*   ExtensionMessageOptions
*   {
*    extension: "myExtension" // binaryName
*    data: "" // Message string
*   }
*
*  ./extensions/bin/myExtension-win.exe
*  ./extensions/bin/myExtension-linux
*  ./extensions/bin/myExtension-mac
*
*  ./extensions/src/myExtension.cpp or ./extensions/src/myExtension.go
*   
*  "neu extensions --build" - Make binaries for all extensions
*  "neu extensions" - Lists existing extensions
*  CLI plugin for neu CLI base
*
*/
```
- Upgrade logging library **(Done)**.
- Implement opposite of `nativeBlockList` as `nativeAllowList` **(Done)**.

## Specs

### window

- `window.minimize()` - **(Done)**
- `window.maximize()` - **(Done)**
- `window.unmaximize()` - **(Done)**
- `window.setFullScreen()` - **(Done)**
- `window.exitFullScreen()` - **(Done)**
- `window.isMaximized()` - **(Done)**
- `window.isFullScreen()` - **(Done)**
- `window.show()` - **(Done)**
- `window.hide()` - **(Done)**
- `window.isVisible()` - **(Done)**
- `window.focus()` - **(Done)**
- `window.setIcon(string icon)` - **(Done)**
- `window.move(int x, int y)` - **(Done)**
- `window.setDraggableRegion(string domElementId)` -  **(Done)**
- `window.setSize(options)` - **(Done)**
- `window.create(url, options)`

### filesystem

- `filesystem.readBinaryFile()` -  **(Done)**
- `filesystem.writeBinaryFile()` -  **(Done)**
- `filesystem.getStats()` - **(Done)**
- `filesystem.copyFile()` - **(Done)**
- `filesystem.moveFile()` - **(Done)**

### events

- `events.onWindowClose` - **(Done)**

### app

- `app.killProcess()` - **(Done)**
- `app.exit(exitCode)` - **(Done)**
- `app.restartProcess(options)`

# Roadmap 2022

- Depends on the community's feature requests and ideas. We'll post a blog post in December 2021 about plans.


