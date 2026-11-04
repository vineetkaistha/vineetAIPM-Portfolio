# Repository context

## What this project is

This repository contains a small, responsive Memory (Concentration) card game. A player flips cards to find matching pairs, aiming to finish with as few moves as possible.

## What it does

- Offers 4x4 and 6x6 grids, using emoji symbols as the matching pairs.
- Tracks moves and elapsed time, and displays a star rating based on moves.
- Shows a completion dialog and lets the player start another game.
- Saves up to five best results in the browser's `localStorage`.
- Supports mouse and keyboard interaction and includes basic ARIA attributes.
- Uses responsive CSS so the grid adapts to smaller screens.

## How it is built

The game is implemented in [`memory-game.html`](./memory-game.html), which contains the page markup, styles, and JavaScript. It uses standard HTML, CSS, and browser JavaScript; there is no framework, build step, backend, or external dependency. Open that file in a browser to play, or serve the repository with a local HTTP server.

The [`README.md`](./README.md) provides the player instructions and a local-server example.

## What the repository stands for

The project is a lightweight, dependency-free example of an accessible, responsive browser game. “Memory Game” describes its purpose. The repository name includes “GHCP,” but the project files do not define what that suffix stands for, so its expansion is unknown from the available documentation.
