# OpenSpace Electron

OpenSpace Electron is a cross-platform desktop AI assistant project built on Electron. The application is intended to provide an AI-assisted workspace with an integrated terminal experience, so users can interact with local tools, project files, command-line workflows, and future AI capabilities from one desktop interface.

The desktop version is planned to support all platforms targeted by Electron distribution workflows, including macOS, Windows, and Linux. Electron documentation: https://www.electronjs.org/docs

## Project vision

OpenSpace Electron will become a desktop AI assistance environment that combines:

- Terminal-first interaction for developer and operator workflows.
- AI assistant features that can reason over workspace context.
- Desktop integration through Electron for macOS, Windows, and Linux.
- A web-based renderer that can evolve into a modern app interface.
- Secure process separation between Electron main, preload, and renderer layers.

## Planned technology stack

Current foundation:

- Electron
- Node.js
- HTML
- npm

Planned stack and supporting tools:

- TypeScript for safer main, preload, renderer, and shared code.
- Next.js for a structured React-based renderer experience.
- Tailwind CSS for utility-first interface styling.
- Electron Forge for packaging, publishing, and cross-platform desktop distribution.
- Additional development tooling for linting, formatting, testing, release automation, and AI-assisted workflows.

## Current project structure

```text
openspace-electron/
├── .vscode/           # VS Code debug configuration
├── src/               # Electron source files
│   ├── main.js        # Electron main process entry
│   └── index.html     # Initial renderer page
├── package.json       # npm metadata and scripts
├── package-lock.json  # npm lockfile
├── .gitignore         # Node/Electron ignore rules
├── LICENSE            # MIT license
└── README.md          # Project documentation
```

## Development

Install dependencies:

```bash
npm install
```

Start the current Electron app shell:

```bash
npm start
```

## Roadmap

- Migrate JavaScript sources to TypeScript.
- Introduce Electron preload and secure IPC boundaries.
- Add a terminal-backed AI assistant interface.
- Add Next.js and Tailwind CSS renderer architecture.
- Configure Electron Forge for packaging and publishing.
- Add test, lint, format, and release workflows.
- Prepare desktop builds for macOS, Windows, and Linux.

## Security direction

As the app evolves, Electron windows should keep secure defaults enabled:

- `contextIsolation: true`
- `nodeIntegration: false`
- `sandbox: true` where practical
- Explicit IPC channel allowlists through preload scripts
- No direct exposure of raw Node.js or Electron APIs to renderer pages

## License

MIT
