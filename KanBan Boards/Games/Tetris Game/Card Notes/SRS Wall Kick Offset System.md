---
Name: SRS Wall Kick Offset System
Created At: 2026-09-06
Due Date:
---
# SRS Wall Kick Offset System

- [ ] **Task 6.1: JLSTZ Kick Offset Tables**
  - Construct standard 5-vector test tables for all 8 rotational transitions ($0 \to 1$, $1 \to 0$, $1 \to 2$, etc.) for $J, L, S, T, Z$ pieces.

- [ ] **Task 6.2: I-Piece Kick Offset Tables**
  - Construct specialized 5-vector kick test tables tailored to the $I$-piece's $4 \times 4$ bounding box and offset pivots.

- [ ] **Task 6.3: Sequential Kick Evaluation Engine**
  - Design the rotation execution sequence:
    1. Apply basic matrix rotation.
    2. Test if valid using `is_valid_position()`. If valid, accept rotation.
    3. If invalid, iterate through the 5 kick vectors sequentially.
    4. Apply the first offset vector that passes spatial validation.
    5. If all 5 offset tests fail, reject the rotation input entirely.

---

### Definition of Done (DoD)
This step is considered **DONE** when:
1. Rotating pieces directly against left/right walls successfully shifts them inward (wall kick).
2. Rotating a $T$-piece in tight floor/block structures executes valid kick tests (e.g., $T$-spin setups).
3. Rotations where all 5 test vectors overlap occupied space are completely cancelled, maintaining the piece's original orientation and position.