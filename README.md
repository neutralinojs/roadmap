# Roadmap 2022

## Native APIs

- Screen details API **(Done)**.
- Global keyboard shortcuts API.
- Get window title via `window.getTitle` **(Done)**.
- Get window size via `window.getSize`. Output the same structure returned with `window.setSize` **(Done)**.
- Set on top mode during the runtime via `window.setAlwaysOnTop(bool)` **(Done)**.
- Get window position via `window.getPosition`. **(Done)**
- Clipboard API **(Done)**
- `os.spawnProcess` for realtime process input and output. **(Done)**
- `filesystem.appendFile` and `filesystem.appendBinaryFile`. **(Done)**
- `filesystem.spawnWatcher` for realtime file events.
- `computer.getArch` to get the user computer's processor architecture. **(Done)**
- `computer.getKernelInfo` to get the user computer's OS kernel details. **(Done)**
- `computer.getOSInfo` to get the user computer's OS details. **(Done)**
- `computer.getCPUInfo` to get the user computer's CPU details. **(Done)**
- `computer.getDisplays` to get the user computer's available displays. **(Done)**
- `os.getEnvs` to get all environment variable details. **(Done)**
- `storage.getKeys` to get all storage keys as a JavaScript array object **(Done)**
- `Neutralino.net` for networking APIs. i.e., `Neutralino.net.fetch`

## Adding custom APIs

Neutralinojs offers the extensions API to write custom backend code with any programming language, but extensions come with the following drawbacks that affect apps in several scenarios:

- Extensions use a shared WebSocket for communication, so using direct C++ references (i.e., the window handler) is impossible within extensions.
- The developer is responsible for packaging their extension binaries.
- A C++-based extension is not fast as native C++-based code due to the WebSockets-based IPC.

Alternatively, a developer can download the framework C++ code, modify it, and re-compile it. But, the developer may face issues while synching upstream code modifications. So, Neutralinojs offers a separate namespace, a function template, inbuilt helper functions (i.e., to get the window handler), and a developer guide to add custom APIs to the Neutralinojs framework without updating the framework core.

Example:

```js
let res = await Neutralino.custom.fetch('https://neutralino.js.org');
```

If developers make a custom API that others can use, we motivate them to contribute to the Neutralinojs framework by adding it to the main codebase.

Example:

```js
let res = await Neutralino.net.fetch('https://neutralino.js.org');
```

## Events

- `windowBlur` and `windowFocus` native events. **(Done)**

## Configuration

- Set startup window position for the window mode.

```
"x": 100,
"y": 100
```
```
"center": true
```
- Set headers for the HTTP responses (static server) and Websocket handshake. This feature is helpful to enable CORS **(Done)**. 
- Chrome mode **(Done)**
- Transparency setting `transparency: bool` in the window configuration section (Developers can control the opacity level with CSS opacity settings).

## Developer Environment

- Support frontend-framework-based hot reloading **(Done)**.

## Archived roadmaps

- [2021](archive/2021.md)
