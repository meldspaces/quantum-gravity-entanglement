## Quantum Entanglement and Gravity

Static Three.js + Pyodide playground visualizing entanglement/gravity interactions. Development happens entirely in the browser: a lightweight HTTP server serves `index.html` and assets so relative URLs and WASM modules load correctly.

### 🟢 Always-on dev server in VS Code

- The workspace now ships with a VS Code task (`.vscode/tasks.json`) that runs `npm start` (http-server on <http://localhost:8080>).
- The task is configured with `runOn: "folderOpen"`, so as soon as you open this folder in VS Code the server spins up and stays alive in the background while VS Code is open.
- A matching Chrome launch config (`.vscode/launch.json`) depends on the same task, ensuring the server is running before the browser debugger launches.

### Usage

1. **Open the folder in VS Code** — the "Start dev server" task launches automatically the first time.
2. **View the app** — open <http://localhost:8080> manually or use the built-in "Launch Chrome against localhost" debugger config.
3. **Stop the server** — run **Terminal → Run Task... → Terminate Task**, then choose "Start dev server" (or press `⌘.` inside the running server terminal).
4. **Restart manually** — run **Terminal → Run Task... → Start dev server** or `npm start` in an integrated terminal.

> Tip: if you prefer to manage the lifecycle yourself, set `"runOn": "default"` in `.vscode/tasks.json` or disable automatic tasks via VS Code's notification.
