# Orbit Archive

An interactive collection of four procedurally drawn orbital plates. Open `index.html` in a current browser. The app runs offline and uses no dependencies.

- Select a plate to compare its colour and orbit geometry.
- Use the viewing angle slider or turn on auto-rotation. The plate stays still until you move it.
- Save a PNG of the current drawing.

The drawing code, text, and graphics were created independently. The project takes inspiration from the broad concept of a navigable spatial gallery. [Concept reference](https://github.com/YildizDikme/3D-threejs-spiral-gallery)

## Local server and agent connection

Install Node 22 or newer and Git. From this repository run:

```sh
npm ci
npm start
```

Open the loopback URL printed by the command. The runtime is pinned to a specific revision of [Project Agent Bridge](https://github.com/Mert-Oezdemir/project-agent-bridge).

To connect an MCP-compatible agent, run `npm run mcp:config --silent` and add its `mcpServers` entry to your host. Run `npm run doctor` to see local project and account configuration.

Chrome or Edge is needed for agent browser controls. You can set `CHROME` in `.env`, or run `npx playwright install chromium` to install a browser.

Copy `.env.example` to `.env` before adding account settings. Keep `.env` local. Restart the runtime after changing it.
