# Roadmap 2022

## Native APIs

- Screen details API.
- Global keyboard shortcuts API.
- Get window title via `window.getTitle` **(Done)**.
- Get window size via `window.getSize`. Output the same structure returned with `window.setSize` **(Done)**.
- Set on top mode during the runtime via `window.setAlwaysOnTop(bool)` **(Done)**.
- Get window position via `window.getPosition`.
- Clipboard API **(Done)**

## Events

- `windowBlur` and `windowFocus` native events.


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
- Transparency level setting `opacity: number` in the window configuration section.

## Developer Environment

- Support frontend-framework-based hot reloading **(Done)**.

## Archived roadmaps

- [2021](archive/2021.md)
