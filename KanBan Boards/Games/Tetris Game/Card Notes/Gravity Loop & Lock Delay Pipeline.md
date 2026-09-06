---
Name: Gravity Loop & Lock Delay Pipeline
Created At: 2026-09-06
Due Date:
---
# Step 7: Gravity Loop & Lock Delay Pipeline

- [ ] **Task 7.1: Gravity Tick Mechanism**
  - Implement a timer-driven step function that moves the active piece down by 1 row ($Y + 1$) on every tick.

- [ ] **Task 7.2: Lock Delay Engine**
  - When the active piece touches a surface below:
    - Start a lock-delay timer (standard $500\text{ms}$).
    - Reset the timer on valid horizontal moves or rotations (up to a maximum reset limit, e.g., 15 moves) to prevent infinite holding.

- [ ] **Task 7.3: Piece Locking & Unparenting**
  - Upon lock delay expiration, unparent active block instances, write their node references directly into the matching $[X, Y]$ playfield array slots, and destroy the container piece node.

---

### Definition of Done (DoD)
This step is considered **DONE** when:
1. Pieces drop continuously at the rate set by the gravity timer.
2. Touching a floor gives the player a $500\text{ms}$ window to slide or rotate before the piece locks into place.
3. Once locked, active block nodes transition into stationary array elements, and a new piece spawns immediately.