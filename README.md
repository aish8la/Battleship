# Battleship Game

This is a web-based Battleship game built with JavaScript, HTML, and CSS. The project focuses on a playable single-player experience, modular code organization, and a responsive interface powered by Webpack.

---

## Features

- Single-player gameplay against a basic computer opponent
- Random ship placement with collision and boundary checks
- Turn-based attack flow across both boards
- Automatic winner detection when a fleet is destroyed
- Dynamic UI updates that reflect the current state of the game
- Clear visual feedback for hits, misses, and sunk ships
- Pub-sub architecture to separate game logic from rendering concerns
- A modular codebase with clear responsibilities across files

---

## Project Structure

```text
src/
├── app.js                # Core game logic: Ship, Gameboard, Player
├── gameFlow.js          # Controls game flow and state transitions
├── displayerController.js # Renders board updates and user-facing states
├── UIController.js      # Handles user interactions and input events
├── pubsub.js            # Event-based messaging system
├── index.js             # Application entry point
├── index.html           # Main page structure
├── style.css            # Layout and board styling
``` 

---

## Development and Build Setup

This project uses a custom Webpack configuration to bundle assets and support local development.

### Install Dependencies

```bash
npm install
```

### Available Scripts

```json
"scripts": {
  "start": "webpack serve --open --config webpack.dev.js",
  "build": "webpack --config webpack.prod.js",
  "lint": "eslint .",
  "format": "prettier --write ."
}
```

| Script | Description |
| --- | --- |
| `start` | Launches the development server |
| `build` | Produces a production-ready bundle |
| `lint` | Runs ESLint for code quality checks |
| `format` | Formats the project with Prettier |

### Production Build

```bash
npm run build
```

This creates a bundled version of the app in the `dist/` directory, which can be served on any static hosting platform.

---

## Game Rules

- Each player controls a 10x10 grid and commands five ships with lengths of 5, 4, 3, 3, and 2.
- Players take turns selecting coordinates to attack.
- Hits, misses, and sunk ships are displayed visually on the board.
- The first player to destroy all enemy ships wins the match.

---

## Planned Improvements

The following features are not currently implemented, but could be added in future iterations:

- [ ] Drag-and-drop ship placement
- [ ] Two-player local mode on the same machine
- [ ] More advanced computer AI with target prioritization
- [ ] Manual ship placement via click interactions
- [ ] Improved in-game status messaging
- [ ] Reset or replay flow for a new match

---

## Author

**Aish Waheed**

---

## License

This project is licensed under the [MIT License](LICENSE).
