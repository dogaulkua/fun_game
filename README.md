# Fun Game

A lightweight browser game built as a single-page app in one HTML file.

## Overview

- Name: **Fun Game**
- Goal: Jump over obstacles and survive as long as possible.
- Features:
  - Increasing speed over time
  - High score tracking using `localStorage`
  - Retry button after game over
  - Funny sound effects for jump, hit, and game over
  - Colorful cartoon-style visuals
  - Parallax scrolling background layers
  - Canvas-only character and obstacle rendering

## Run

1. Open `index.html` in a modern browser.
2. Use **Space**, **ArrowUp**, or tap/click the game area to jump.
3. Avoid obstacles and try to beat the high score.
4. Press **Retry** after game over to play again.

## Notes

- No build step is required.
- The game is implemented entirely in `index.html`.
- High score persists in the browser using `localStorage`.
- If audio is blocked or unavailable, the game remains playable.

## Repository

The feature spec and implementation artifacts are stored under `specs/001-fun-game/`.
