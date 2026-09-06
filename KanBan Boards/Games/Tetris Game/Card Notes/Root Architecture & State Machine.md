---
Name: Root Architecture & State Machine
Created At: 2026-09-06
Due Date:
---
# Step 1: Root Architecture & State Machine

- [ ] **Task 1.1: Top-Level Node Ownership**
  - Design `Main` as the top-level game orchestrator managing state transitions and cross-system communication.
  - Isolate `Board` as a dedicated 2D spatial container managing the $10 \times 20$ playfield grid and active piece instances.
  - Isolate `HUD` as an event observer responsible solely for visual presentation.

- [ ] **Task 1.2: Finite State Machine (FSM) Design**
  - Implement an explicit state machine on `Main` with state handlers:
    - `INIT`: Clears grid memory, resets scores, seeds random generators.
    - `SPAWN`: Fetches next piece from queue, sets spawn position $(4, 0)$, validates immediate spawn collisions.
    - `PLAYING`: Enables gravity timers and accepts player inputs.
    - `LOCKING`: Manages lock-delay grace periods when piece touches a floor or block.
    - `CLEARING`: Scans for completed rows, runs line-removal sequences, collapses upper rows.
    - `GAME_OVER`: Disables player input, stops timer loops, emits loss events.

- [ ] **Task 1.3: Game Loop Data Flow**
  - Establish unidirectional pipeline: User Input $\to$ `Board` (Validate/Execute) $\to$ `FSM State Change` $\to$ Signal Emission $\to$ `HUD` Render.

---

### Definition of Done (DoD)
This step is considered **DONE** when:
1. Running `Main` cleanly initializes all subsystems without null references or orphaned instances.
2. Every state in the FSM can be explicitly logged with va11lid entering and exiting transitions.
3. Transitioning to `GAME_OVER` immediately halts player input and gravity timers, while transitioning to `INIT` fully resets the state without requiring a full scene reload.