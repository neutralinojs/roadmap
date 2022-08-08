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
- `os.getEnvs` to get all environment variable details.

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
