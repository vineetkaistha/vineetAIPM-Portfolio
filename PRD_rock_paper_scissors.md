# Product Requirements Document: Rock, Paper, Scissors

## Summary

Create a standalone Rock, Paper, Scissors game as one HTML file using plain
HTML, CSS, and JavaScript. A player chooses a move, the computer chooses a move,
and the game explains the result. The first side to win three rounds wins the
match.

## Goals

- Make it quick to understand and play on desktop and mobile.
- Let the player choose Rock, Paper, or Scissors using accessible controls.
- Clearly show both moves, the round result, and the match score.
- Keep the game self-contained, responsive, and usable without network access.

## Non-goals

- Multiplayer, accounts, online leaderboards, or network access.
- AI opponent, difficulty levels, or strategic adaptation.
- Configurable rules, tournament brackets, or additional game modes.
- External libraries, images, fonts, or build tools.

## Rules and match flow

- Rock beats Scissors, Scissors beats Paper, and Paper beats Rock.
- The computer selects one of the three moves at random for every player turn.
- A match is first to three round wins.
- A tie does not award a point and does not move either score.
- After each choice, display both moves and explain whether the player won,
  lost, or tied.
- Once either side reaches three wins, announce the match winner and disable
  move selection until the player starts another match.
- Starting a new match resets both scores and the round message.

## Interface and interaction

- Provide clearly labeled Rock, Paper, and Scissors buttons with visible text
  and simple built-in emoji or text symbols.
- Display the player's choice and the computer's choice for the most recent
  round.
- Show the player and computer scores, with the target of three wins.
- Provide a persistent New Match action that resets the match.
- Do not require a separate start screen; the player can choose a move
  immediately after loading the page.

## Accessibility and design

- Use native buttons with descriptive accessible names and visible focus
  indicators.
- Announce round results and match completion through a polite live region.
- Do not communicate the result with color alone; include clear result text.
- Keep controls and score readable on narrow screens.
- Respect the system light/dark color preference and reduced-motion preference.
- Ensure all game interactions work with keyboard, mouse, and touch.

## Technical requirements

- Put all markup, styles, and game logic in `rock-paper-scissors.html`.
- Use only standard browser HTML, CSS, and JavaScript.
- Keep the game functional when opened directly from disk, with no server,
  build step, external asset, or dependency.
- Keep scores in the current page session only; do not read or modify the
  Memory Game or Snake score data.

## Acceptance criteria

1. The game loads directly in a modern browser without network access.
2. The player can choose any move with mouse, keyboard, or touch.
3. Each round displays the player's choice, computer choice, and correct
   outcome according to the rules.
4. A win increments only the player's score; a loss increments only the
   computer's score; a tie increments neither.
5. The match ends when either score reaches three, identifies the match winner,
   and prevents additional moves until reset.
6. New Match resets both scores and allows play immediately.
7. Round and match messages are announced to assistive technology, and controls
   have visible keyboard focus.
8. The layout remains readable and operable on mobile and desktop, in light and
   dark system themes.
9. Motion is reduced or removed when the user requests reduced motion.
10. Existing game files and their score storage remain unchanged.

## Manual verification checklist

- Open `rock-paper-scissors.html` directly in a browser.
- Play wins, losses, and ties; verify choices, messages, and scores.
- Reach three wins for either side; confirm the match ends and choices disable.
- Start a new match and confirm the score and state reset.
- Use Tab and Enter/Space to play; check focus and screen-reader status text.
- Test at narrow mobile width and in light and dark system themes.
- Enable reduced motion and confirm no necessary information depends on motion.
- Confirm Memory Game and Snake files and their saved scores are unaffected.
