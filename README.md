The roadmap of Neutralinojs

# Roadmap 2021

- Refactoring macOS version for v2 using core-shared APIs.  **(Done)**.
- Set exit code for `app.exit()` from JavaScript API. **(Done)**
- Doing improvements to the window customization (via `neutralino.config.json`).
  * `minHeight`, `minWidth`, `maxWidth`, `maxHeight`, and `resizable` **(Done)**.
  * `hidden: boolean` - A nice way to write background apps. **(Done)**
- `enableHTTPServer: boolean` and `enableNativeAPI: boolean` Useful when setting a remote URL for the entry URL property. **(Done)**
- Implement a way to change the path context via command line. Keep Neutralino binaries without renaming inside the `bin` directory.  **(Done)**
- Adding new methods to the native API.
  * `async filesystem.readBinaryFile`, `async filesystem.writeBinaryFile`, `async filesystem.getStats` and `async filesystem.copyFile` - **(Done)**
  * GUI manipulation methods. Eg: `window.setTitle(string title)` etc. **(Done)**
  * Tray menu API `async os.setTrayMenu()`. **(Done)**
  * `Neutralino.events`. Centralized namesapce for native events. **(Done)**
- Neutralino API extensions - Developers can make their own backend code with any programming language. STDIN/STDOUT is used as the communication channel. This feature allows devs to use Nodejs too.
- Upgrade logging library **(Done)**.
- Implement opposite of `nativeBlockList` as `nativeAllowList` **(Done)**.
- Add a new setting (also command line flag) to enable/disable log file/logging. **(Done)**
- Performance improvements and optimizations.


## Specs: API (Done)

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
- `window.create(url, options)` - **(Done)**

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
- `app.restartProcess(options)` - **(Done)**

### os

- `os.getPath(name)` - **(Done)**

## Specs: Error codes (Done)

Format: `NE_<namespace_shortcode>_<error_in_seven_letters>`

- `NE_FS_DIRCRER` - Unable to create directory.
- `NE_FS_RMDIRER` - Unable to remove directory.
- `NE_FS_FILRDER` - File read error.
- `NE_FS_FILWRER` - File write error.
- `NE_FS_FILRMER` - File remove error.
- `NE_FS_NOPATHE` - No file or directory.
- `NE_FS_COPYFER` - File copy error.
- `NE_FS_MOVEFER` - File move error.
- `NE_OS_ENVNOEX` - The environment variable is not defined.
- `NE_OS_INVMSGA` - Invalid message box arguments.
- `NE_OS_INVKNPT` - Invalid platform path name.
- `NE_ST_INVSTKY` - Invalid storage key.
- `NE_ST_STKEYWE` - Storage write error.
- `NE_RT_INVTOKN` - Invalid auth token.
- `NE_RT_NATPRME` - No permission to execute the provided native method.
- `NE_RT_APIPRME` - No permission to use the native API.
- `NE_RT_NATRTER` - Native method runtime error.
- `NE_RT_NATNTIM` - Native method is not implemented.
- `NE_CL_NSEROFF` - Neutralino server is not reachable.
- `NE_EX_EXTNOTC` - Extension is not connected yet.

## Specs: API extensions (Done)

- Extension to/from Neutralinojs process communication: WebSocket
- JavaScript API to invoke extension:

```js
await Neutralino.extensions.dispatch(string extensionId, string event, string data);
```
- Which component initates extensions: Server process.
- Config extensions:

```js
"extensions": [
 {
  id: "js.neutralino.extension1",
  command: "python {NL_PATH}/extensions/ext1.py" // Internal args: --nl-port={}, --nl-token={}
  // commandLinux, commandDarwin, and commandWindows are also supported.
 }
]
```

- neu CLI behavior for extensions.

`neu build` will copy extensions dir to the bundle based on the following setting. `res.neu` won't include extensions.
```js
"cli": {
   "extensionsPath": "/extensions/"
}
```

## Devops (Done)

Release pre-built binaries for x64 Linux, macOS, and Windows via GitHub actions. If developers needs binaries for other CPU archirectures, they have to build from source. Add build from source guide to docs.

- `create_release_zip.yml`: Build binaries, Add to zip, and place zip file in `bin/`. Commit the zip file automatically. But, the final release is manual. **(Done)**
- `test_suite.yml`: Build binaries first. Execute integration test suite and run it with code changes.

# Roadmap 2022

- Screen details API.
- Transparency level setting `opacity: number` in the window setting section.

- Depends on the community's feature requests and ideas. We'll post a blog post in December 2021 about plans.


