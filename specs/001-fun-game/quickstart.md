# Quickstart: Fun Game

## Run the game

1. Open `index.html` in a modern browser.
2. Use the **space bar**, **up arrow**, or **click/tap** anywhere on the page to make the player jump.
3. Avoid obstacles as they approach from the right side of the screen.
4. When the game ends, press the **Retry** button to restart.

## What to look for

- A colorful cartoon-style background with at least two independently moving parallax layers.
- A central game canvas showing the player, obstacles, and the ground.
- A visible score display and a high score indicator.
- Funny sound effects for jump actions, collisions, and game over events.
- The game should still work if audio is unavailable.

## Persistence

- The high score is stored in browser `localStorage` and should remain available after page reloads in the same browser profile.

## Notes

- Because this feature is a single HTML file, no build step is required.
- If the browser blocks audio playback, the game should continue running without sound.
