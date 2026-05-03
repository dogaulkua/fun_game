# UI Contract: Fun Game

## Purpose

This contract defines the user-facing interface and interactions for the Fun Game browser page.

## Page Contract

### Required UI sections

- **Parallax background**: The page must present at least two visually distinct layers that move at different speeds to create depth.
- **Game canvas**: A central Canvas element must render the player character, obstacles, ground, and any simple decorative shapes.
- **Score display**: The current score and high score must be visible during gameplay.
- **Retry button**: A clearly labeled retry control must be available after game over.

### Controls

- **Jump action**: The user must be able to initiate a jump using:
  - keyboard: `Space` or `ArrowUp`
  - mouse click / tap anywhere on the screen
- **Retry action**: The user must be able to restart the game by pressing the on-screen retry button.

### Behavior

- **Gameplay**: The game starts immediately after the first jump or tap, and the player should be able to keep playing until collision with an obstacle.
- **Speed**: Obstacle speed and difficulty must increase over time to make the run progressively harder.
- **Scoring**: The current score updates continuously while the game is running; the high score updates after a run completes if the new score is higher.
- **Audio**: Funny sound effects should play for jump, collision, and game-over events when audio is available; the interface should still function without sound.

### Failure modes

- If audio playback is blocked, the game still advances, displays score updates, and shows the retry button after game over.
- If localStorage is unavailable, the game still runs but high score persistence may not be saved.

## Acceptance

This contract is satisfied when the page delivers a complete browser game experience in one HTML file with the required UI sections, controls, and persistence behavior.
