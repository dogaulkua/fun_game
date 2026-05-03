# Research: Fun Game

## Decision: Native browser single-page game

- **Chosen**: Build the game as a single HTML file using native browser APIs.
- **Rationale**: The requirement explicitly asks for a single-page app in one HTML file. Native APIs avoid external dependencies and support fast browser delivery.
- **Alternatives considered**: separate JS/CSS files, modules, or a framework-based approach, but these violate the single-file requirement.

## Decision: Canvas API for rendering

- **Chosen**: Use the Canvas API for game rendering.
- **Rationale**: Canvas provides precise control over animated shapes and is a standard way to build browser games without relying on external assets.
- **Alternatives considered**: DOM elements with CSS transforms (rejected because Canvas better supports fast shape-based graphics and obstacle rendering for this game).

## Decision: CSS animations for parallax backgrounds

- **Chosen**: Use CSS animations to drive background layer motion.
- **Rationale**: CSS animations are efficient for repeating parallax movement and cleanly separate background motion from the Canvas gameplay loop.
- **Alternatives considered**: drawing background movement in Canvas (rejected because the requirement explicitly calls out CSS animations for parallax layers and it simplifies layering).

## Decision: Web Audio API for sounds

- **Chosen**: Use Web Audio API for sound effects.
- **Rationale**: Web Audio gives solid control over small sound effects without external audio libraries and works in modern browsers.
- **Alternatives considered**: HTMLAudioElement or external sound libraries (rejected because Web Audio is more flexible for generated or inline sound effects and does not require assets).

## Decision: localStorage for high score persistence

- **Chosen**: Persist the high score in browser localStorage.
- **Rationale**: localStorage is available in the target platform, simple to use, and fits the session persistence requirement without backend storage.
- **Alternatives considered**: cookies or server storage (rejected because localStorage is easier and more appropriate for a standalone single-page browser game).

## Decision: Canvas shapes only, no images

- **Chosen**: Draw the player, obstacles, and simple scenery using Canvas shape primitives only.
- **Rationale**: It satisfies the no-images requirement and keeps the implementation self-contained.
- **Alternatives considered**: using inline SVG or data-URI images (rejected because the requirement specifies Canvas shapes and no images).
