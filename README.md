# Roadmap 2024

## Native APIs

- Global keyboard shortcuts API.
- New window events.
- Add a way to inject custom script into remote URLs on the window mode. **(Done)**
- Consider `storageLocation` while creating app-specific files within the app directory.
- `Neutralino.net` for networking APIs. i.e., `Neutralino.net.fetch`
- Introduce an event system for multi-window communication.
- Add new functions `resources.getFiles()`, `resources.readFile(path)`, `resources.readBinaryFile(path)`, and `resources.extractFile(path, destination)` to let developers parse the `resources.neu` file. **(Done)**

## Extensions

- Introduce a way to debug extensions on Windows by displaying stdout/stderr on the terminal.

## Configuration

- Add `window.transparent` boolean config property (default is `false`) to enable window transparency (Developers can control the opacity level with CSS using `rgba` color function). **(Done)**
- Configless framework initialization. **(Done)**

## Static server

- Single Page App (SPA) serving support can be acticated using the `singlePageServe` boolean configuration option. **(Done)**

## Documentation

- Application distribution guidelines with the [Neutralinojs build scripts community project](https://github.com/hschneider/neutralino-build-scripts), see [this reference](https://github.com/neutralinojs/neutralinojs/issues/1152#issuecomment-1859653388). **(Done)**
- A page with Neutralinojs community tools, learning resources, and templates. **(Done)**
- Update the sample apps page with new community apps. **(Done)**
  
## Archived roadmaps

- [2023](archive/2023.md)
- [2022](archive/2022.md)
- [2021](archive/2021.md)
