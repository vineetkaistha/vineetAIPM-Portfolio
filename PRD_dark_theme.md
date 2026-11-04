# Product Requirements Document: Dark Theme

## Summary

Add an optional dark appearance to the existing Memory Game. Players should be able to switch between light and dark themes, with their choice remembered between visits. The feature must work within the existing single-file HTML/CSS/JavaScript implementation and must not change gameplay, scoring, or the current light-theme experience.

## Goals

- Let players choose light or dark mode with a clearly visible control.
- Remember a player's explicit theme choice across page reloads.
- Provide a sensible initial theme based on the operating system when no choice has been saved.
- Keep all game content readable and usable on desktop and mobile, with mouse and keyboard.
- Preserve the existing game behavior, appearance in light mode, and saved scores.

## Non-goals

- Changing game rules, card symbols, grid sizes, animations, ratings, or score ranking.
- Adding a framework, build step, backend, or external dependency.
- Adding additional themes or a broader settings panel.

## User experience

1. On first visit, use the browser's `prefers-color-scheme` preference to choose light or dark mode. If that preference is unavailable, use light mode.
2. Provide a theme toggle near the existing grid-size controls. It must identify the action or destination clearly (for example, “Switch to dark theme” in light mode and “Switch to light theme” in dark mode).
3. When toggled, update the page immediately without resetting the current game, timer, moves, rating, or selected grid.
4. Save the explicit choice using a dedicated local-storage key, separate from `memoryGameScores`. On later visits, the saved choice takes precedence over the system preference.
5. If the saved value is missing or invalid, fall back to the system preference rather than failing to render the game.

## Functional requirements

- Implement both themes in the existing `memory-game.html` file, following its current structure and no-dependency approach.
- Use CSS custom properties (or the existing equivalent) for theme-dependent colors so all relevant surfaces switch consistently.
- Apply the selected theme to the page background, text, controls, game cards, score panel, and win dialog, including their borders, shadows, and interactive states where applicable.
- Preserve card-face contrast and the existing flip/match behavior in both themes.
- Keep the theme control operable by keyboard, with a visible focus indicator and an accessible name that reflects its action or current state.
- Persist only the theme preference; do not overwrite, clear, or alter existing score data.
- If local storage is unavailable, the game and theme control must remain usable for the current page session.
- Avoid flashes of the wrong theme on initial render where practical; theme initialization must not delay or prevent game initialization.

## Design and accessibility

- Retain the current light theme's colors and appearance as the default fallback.
- Use a distinct, readable palette for dark mode; do not rely on color alone to communicate focus, matched cards, or control state.
- Maintain readable contrast for text, buttons, card faces, focus outlines, and modal content in both themes.
- Keep the layout responsive and the theme control usable at narrow viewport widths.
- Respect reduced-motion preferences if theme transitions are animated; transitions must not interfere with card animations.

## Compatibility and safeguards

- Do not change the existing game-state flow or reset the board when changing themes.
- Keep the existing `memoryGameScores` storage format and best-score display intact.
- Keep the 4x4 and 6x6 selectors, card keyboard controls, timer, rating, completion modal, and Play Again action working as before.
- Do not introduce external assets, libraries, or network requirements.

## Acceptance criteria

1. With no saved preference, the game starts in the operating-system theme; when that preference cannot be read, it starts in light mode.
2. The theme control switches between light and dark immediately and remains usable with mouse, Enter, and Space.
3. Reloading after choosing a theme restores that theme, even if the operating-system preference differs.
4. Changing themes during an active game leaves the current cards, grid size, move count, timer, rating, and match progress unchanged.
5. All game areas, including the cards, controls, score list, and win dialog, remain legible and usable in both themes at desktop and mobile widths.
6. Existing game interactions and scoring continue to work in both themes, including keyboard card flips, both grid sizes, winning, and Play Again.
7. Existing best scores remain available after changing themes; the theme preference is stored separately from score data.
8. If storage is unavailable or contains an invalid theme value, the game still loads and can be played.
9. The original light-theme experience remains visually and functionally unchanged apart from the addition of the theme control.

## Manual verification checklist

- Open `memory-game.html` in a browser with the system set to light, then dark, without a saved theme preference.
- Toggle each theme using both mouse and keyboard; verify the control's accessible name and visible focus.
- Reload after selecting each theme and confirm the selection persists.
- Start a game, change themes mid-game, and check that the board and all statistics remain unchanged.
- Test both grid sizes, matches and mismatches, the timer, rating, completion dialog, and Play Again in both themes.
- Check the score list and confirm existing best scores remain after theme changes and reloads.
- Resize to a narrow viewport and check text contrast and control usability in both themes.
- With browser storage blocked or unavailable, confirm the game still initializes and can be played.
