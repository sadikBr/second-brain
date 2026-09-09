---
Name: Spatial Collision & Boundry Engine
Created At: 2026-09-06
Due Date:
---
# Spatial Collision & Boundary Engine

- [ ] **Task 5.1: Boundary Query Algorithm**
  - Design a validation algorithm `is_valid_position(cells, target_position) -> bool`.
  - Check horizontal limits ($0 \le X < 10$) and floor limits ($Y < 20$).
  - Allow negative Y coordinates ($Y < 0$) to support the hidden buffer zone above the visible board.

- [ ] **Task 5.2: Matrix Occupancy Validation**
  - Cross-reference absolute cell coordinates against the playfield memory array.
  - Return `false` if any cell in the target shape overlaps a non-null entry in the spatial array.

- [ ] **Task 5.3: Predictive Movement Queries**
  - Structure movement functions to execute query checks *prior* to modifying active piece coordinates, rejecting invalid translations seamlessly.

---

### Definition of Done (DoD)
This step is considered **DONE** when:
1. Pieces cannot move past the left ($X=0$), right ($X=9$), or bottom ($Y=19$) board boundaries.
2. Pieces correctly register collisions against placed blocks in the spatial array and reject overlapping moves.
3. Spawning or rotating pieces in the $Y < 0$ buffer zone evaluates correctly without throwing index-out-of-bounds errors.