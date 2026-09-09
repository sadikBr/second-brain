---
Name: Ghost Projection, Hold & Hard Drop
Created At: 2026-09-06
Due Date:
---
# Ghost Projection, Hold & Hard Drop

- [ ] **Task 10.1: Real-Time Ghost Projection**
  - Calculate landing position on every frame: clone active piece position and project downward ($Y + 1$) until `is_valid_position()` returns false.
  - Render a semi-transparent outline of the active piece at the calculated ghost position.

- [ ] **Task 10.2: Hard Drop Execution**
  - Instantly move active piece to the calculated ghost position on `hard_drop` input.
  - Bypass lock delay timer and trigger immediate piece locking.

- [ ] **Task 10.3: Hold Piece Architecture**
  - Maintain a `held_piece_type` variable and a `has_swapped_this_turn` boolean flag.
  - Swapping logic:
    - If empty: stash active piece type, despawn active piece, spawn next from queue.
    - If occupied: swap active piece type with held type, reset position to spawn coordinates $(4, 0)$.
    - Set `has_swapped_this_turn = true` until the new piece locks.

---

### Definition of Done (DoD)
This step is considered **DONE** when:
1. The ghost piece dynamically updates its landing position instantly whenever the active piece moves or rotates.
2. Triggering a hard drop places and locks the piece instantly at the ghost location without delay.
3. The hold feature allows swapping pieces once per turn, blocking repeated swaps until the current piece is locked.