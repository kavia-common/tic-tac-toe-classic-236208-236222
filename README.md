# Tic Tac Toe (React Frontend)

This repository contains a single frontend container, `tic_tac_toe_frontend`, which serves a web UI for a simple Tic Tac Toe application.

## Features

The intended application behavior for this work item is a classic Tic Tac Toe experience with a retro-themed presentation. The app is expected to provide a playable 3x3 board, two-player alternating turns (X and O), win/draw detection, and a reset option, with a responsive layout suitable for mobile and desktop.

At the time of writing, the frontend codebase is a lightweight React (Create React App) scaffold that includes a light/dark theme toggle and standard CRA starter content.

## Repository Structure

This repo is organized as a workspace containing the frontend container:

- `tic_tac_toe_frontend/`: React frontend (Create React App)

## Running via Kavia Preview

The frontend container is exposed via the Kavia preview system on port 3000.

- Preview URL: `https://vscode-internal-23525-qa.qa01.cloud.kavia.ai:3000`
- Port: `3000`

If the preview system is already running the container, you can typically refresh the preview URL after making changes to see updates.

## Local Development

### Prerequisites

- Node.js (LTS recommended)
- npm

### Install dependencies

From the container directory:

```bash
cd tic_tac_toe_frontend
npm install
```

### Start the dev server

```bash
cd tic_tac_toe_frontend
npm start
```

By default, Create React App serves the app at:

- `http://localhost:3000`

### Build for production

```bash
cd tic_tac_toe_frontend
npm run build
```

This produces an optimized build in `tic_tac_toe_frontend/build/`.

### Run tests

```bash
cd tic_tac_toe_frontend
npm test
```

Note: CRA’s default `npm test` runs in watch mode. In CI environments, set `CI=true` when running tests.

## Environment Variables

The `tic_tac_toe_frontend` container supports the following `.env` keys (all are optional unless your deployment requires them). These variables are read at build/start time by Create React App when prefixed with `REACT_APP_`.

### API / URL configuration

- `REACT_APP_API_BASE`: Base URL for API calls (if the frontend is configured to call an API).
- `REACT_APP_BACKEND_URL`: Backend service URL (if applicable).
- `REACT_APP_FRONTEND_URL`: Public URL of the frontend (if applicable).
- `REACT_APP_WS_URL`: WebSocket URL (if applicable).

### Runtime and build flags

- `REACT_APP_NODE_ENV`: App environment identifier (separate from Node’s own `NODE_ENV`).
- `REACT_APP_NEXT_TELEMETRY_DISABLED`: Telemetry flag (kept for compatibility; not specific to CRA).
- `REACT_APP_ENABLE_SOURCE_MAPS`: Enables/disables source maps (behavior depends on how the build is configured).
- `REACT_APP_PORT`: Port override for local serving (commonly `3000` in this workspace).
- `REACT_APP_TRUST_PROXY`: Proxy trust flag (only relevant if the frontend is served behind a proxy with special handling).
- `REACT_APP_LOG_LEVEL`: Logging verbosity control (only relevant if app code reads it).
- `REACT_APP_HEALTHCHECK_PATH`: Health check path (only relevant if app code reads it).
- `REACT_APP_FEATURE_FLAGS`: Feature flag configuration string (only relevant if app code reads it).
- `REACT_APP_EXPERIMENTS_ENABLED`: Enables experimental features (only relevant if app code reads it).

If you add or change environment variables, you generally need to restart `npm start` for CRA to pick them up.

## Development Notes

The frontend uses Create React App with the standard scripts defined in `tic_tac_toe_frontend/package.json`:

- `npm start`: start development server
- `npm run build`: create production build
- `npm test`: run tests
- `npm run eject`: CRA eject (not recommended unless you explicitly need it)

Styling is currently handled with plain CSS files under `tic_tac_toe_frontend/src/` (for example, `src/App.css`).

## License

No license file is currently included in this repository.
