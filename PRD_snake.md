# Product Requirements Document: Snake

## Summary

Create a playable, responsive Snake game as a single standalone HTML file using plain HTML, CSS, and JavaScript. The game should work when opened directly in a modern browser, without a build step, external assets, or network access.

## Goals

- Let a player start, pause, resume, and restart a Snake game.
- Support keyboard play on desktop and visible touch controls on mobile.
- Show the current score and preserve the best score when browser storage is available.
- Provide clear game-over and board-complete states.
- Keep the layout readable and usable on small and large screens.

## Non-goals

- Multiplayer, online leaderboards, accounts, or networking.
- External libraries, images, fonts, or build tools.
- Multiple boards or user-configurable game rules.

## Gameplay

- Use a 24-by-24 square grid.
- The snake starts near the center, moving to the right.
- Each food item increases the score by 10 and lengthens the snake by one segment.
- The snake loses when it hits a wall or itself.
- The game is won if the snake fills all available board cells.
- Increase the movement speed gradually as the score rises, up to a safe maximum.
- Do not allow the snake to reverse directly into itself. Ignore invalid reverse turns.

## Controls and states

- Start with the Start Game button; allow restarting at any time.
- On desktop, use Arrow keys or W/A/S/D to steer. Space pauses or resumes.
- On touch screens, provide labeled directional buttons and support swiping on the board.
- States are ready, running, paused, game over, and won. Make the current state clear to the player.
- Ignore repeated key events and prevent arrow keys from scrolling the page during play.

## User experience and accessibility

- Display score, best score, and current game status.
- Provide accessible names for controls, visible keyboard focus, and a live status message for important state changes.
- Keep the board square and responsive, with a visual grid and clear contrast between the snake, its head, and food.
- Respect the operating system's light/dark preference.
- Ensure that the primary game controls remain available to keyboard and touch users.

## Persistence and compatibility

- Save only the best score under a dedicated local-storage key.
- If storage is unavailable or invalid, keep the game playable and use a session-only best score.
- Keep all markup, styles, and game logic in `snake-game.html`.
- Do not alter the existing Memory Game or its score data.

## Acceptance criteria

1. `snake-game.html` opens and plays without a server, dependencies, or network access.
2. The player can start, pause, resume, and restart games.
3. Arrow keys, W/A/S/D, directional buttons, and board swipes steer the snake.
4. Food increases score and snake length; walls and self-collisions end the game.
5. Reversing into the snake is prevented, including when turns are entered quickly.
6. The speed increases as the score grows but does not become unplayable.
7. The best score persists where storage is available, without blocking play when it is not.
8. The board and controls fit narrow screens and remain operable using keyboard or touch.
