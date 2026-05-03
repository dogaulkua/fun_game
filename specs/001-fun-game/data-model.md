# Data Model: Fun Game

## Entities

### GameState

Represents the current running state of the game.

- **currentScore**: number — points accumulated in the current run
- **highScore**: number — highest score stored in localStorage for the session
- **speed**: number — current obstacle / game speed multiplier
- **isRunning**: boolean — whether the game loop is active
- **isGameOver**: boolean — whether the last run ended in failure
- **lastUpdate**: number — timestamp of the last animation frame
- **nextObstacleAt**: number — time threshold for spawning the next obstacle

### Player

Represents the character under player control.

- **x**: number — horizontal position on the canvas
- **y**: number — vertical position on the canvas
- **width**: number — horizontal size of the collision box
- **height**: number — vertical size of the collision box
- **velocityY**: number — current vertical speed
- **isJumping**: boolean — whether the player is currently airborne

### Obstacle

Represents one obstacle in the game world.

- **x**: number — horizontal position on the canvas
- **y**: number — vertical position on the canvas
- **width**: number — width of the obstacle shape
- **height**: number — height of the obstacle shape
- **speed**: number — horizontal speed at which it moves left

### BackgroundLayer

Represents a parallax layer in the page design.

- **speedFactor**: number — relative speed of the layer compared to the foreground
- **color**: string — fill or gradient used by the layer
- **animationName**: string — CSS animation controlling its movement
- **zIndex**: number — stack order to preserve depth

### SoundEffect

Represents an audio event for game actions.

- **name**: string — action name such as `jump`, `hit`, `gameOver`
- **enabled**: boolean — whether sound can currently play
- **volume**: number — playback gain level
- **sourceType**: string — `oscillator` or `buffer` for effect generation

## Persistence

- **highScore** is saved to browser `localStorage` under a key like `funGameHighScore`.
- No other game state is persisted between page reloads.

## Behavior

- Game state updates are triggered by the Canvas animation loop and player input events.
- Collision detection is done against the player and obstacle bounding boxes.
- Score updates continuously while the game is running and increases faster as speed increases.
