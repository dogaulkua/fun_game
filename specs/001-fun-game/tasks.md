# Tasks: Fun Game

**Input**: Design documents from `/specs/001-fun-game/`
**Prerequisites**: plan.md, spec.md, research.md, data-model.md, contracts/

## Phase 1: Setup (Shared Infrastructure)

**Purpose**: Create the single-page game container and base page layout.

- [x] T001 Create `index.html` with a page shell containing the parallax background sections, the game canvas element, the score display, and the retry button
- [x] T002 Add base CSS layout and styling in `index.html` so the page is centered, colorful, and ready to host the game canvas

---

## Phase 2: Foundational (Blocking Prerequisites)

**Purpose**: Build the core game infrastructure that all user stories require.

- [x] T003 Add the Canvas rendering context, initial game state objects, and `localStorage` high score persistence helpers in `index.html`
- [x] T004 Add keyboard and click/touch jump input handlers in `index.html`
- [x] T005 Add the main animation loop, game start logic, game over state, and reset scaffolding in `index.html`

---

## Phase 3: User Story 1 - Start and survive with jumping controls (Priority: P1)

**Goal**: Deliver the playable jump-and-survive core game loop.

**Independent Test**: Open `index.html`, use jump input, avoid obstacles, and verify the game ends on collision while the score increases.

- [x] T006 [US1] Implement the player character as a Canvas shape with jump physics, gravity, and ground collision in `index.html`
- [x] T007 [US1] Implement obstacle spawning, movement, speed escalation, and collision detection in `index.html`
- [x] T008 [US1] Implement the current score calculation and live score display update in `index.html`

---

## Phase 4: User Story 2 - Track high score and retry quickly (Priority: P2)

**Goal**: Add persistent session high score tracking and a retry flow.

**Independent Test**: Complete a run, verify high score updates if exceeded, then use retry to restart the game.

- [x] T009 [US2] Implement session high score persistence in `localStorage` and display the high score in `index.html`
- [x] T010 [US2] Implement the retry button behavior and game reset flow in `index.html`

---

## Phase 5: User Story 3 - Enjoy colorful cartoon visuals and funny sounds (Priority: P3)

**Goal**: Add the fun visual and audio polish required by the game experience.

**Independent Test**: Confirm the page has at least two animated parallax layers, cartoon-style Canvas visuals, and funny sound effects for actions and events.

- [x] T011 [US3] Implement cartoonish player and obstacle visuals using Canvas shapes only in `index.html`
- [x] T012 [US3] Implement Web Audio API sound effects for jump, collision, and game over, with fallback behavior when audio is unavailable in `index.html`
- [x] T013 [US3] Implement colorful CSS animated parallax background layers in `index.html`

---

## Phase 6: Polish & Cross-Cutting Concerns

**Purpose**: Validate the final experience, improve performance, and align docs/contracts.

- [ ] T014 [P] Review and fine-tune animation timing, physics pacing, and frame rendering in `index.html`
- [ ] T015 [P] Validate the game against `specs/001-fun-game/quickstart.md`
- [ ] T016 [P] Confirm `specs/001-fun-game/contracts/ui-contract.md` reflects the final UI behavior and update it if needed
- [ ] T017 [P] Update `specs/001-fun-game/quickstart.md` with any final control guidance and sound/browser compatibility notes

---

## Dependencies & Execution Order

### Phase Dependencies

- **Setup (Phase 1)**: No dependencies, can start immediately
- **Foundational (Phase 2)**: Depends on Phase 1 completion
- **User Story 1 (Phase 3)**: Depends on Phase 2 completion
- **User Story 2 (Phase 4)**: Depends on Phase 2 and the baseline gameplay from Phase 3
- **User Story 3 (Phase 5)**: Depends on Phase 2 and the baseline gameplay from Phase 3
- **Polish (Phase 6)**: Depends on completion of all user stories

### User Story Dependencies

- **US1**: Core gameplay must be implemented first
- **US2**: Builds on the core game loop for score persistence and retry
- **US3**: Builds on the core game loop for visuals and audio polish

## Parallel Execution Examples

- T014, T015, T016, and T017 can run in parallel because they validate and document the final experience rather than changing the same gameplay code.
- Once core gameplay exists, US2 and US3 work can be developed in parallel by focusing on persistence/retry and visual/audio polish separately.
- Setup tasks T001 and T002 should complete before foundational game logic begins.

## Implementation Strategy

1. Complete Phase 1 and Phase 2 to establish the single-file page, Canvas setup, and game loop.
2. Deliver User Story 1 first as the MVP: jumping, obstacles, and scoring.
3. Add User Story 2 for persistence and retry behavior.
4. Add User Story 3 for the colorful cartoon visuals and funny sounds.
5. Finish with Phase 6 validation, performance tuning, and contract alignment.
