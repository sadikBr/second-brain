---
Name: Score Engine & Level Curve Scaling
Created At: 2026-09-06
Due Date:
---
# Score Engine & Level Curve Scaling

- [ ] **Task 11.1: Line Clear Scoring Calculation**
  - Award points based on cleared lines per step:
    - Single (1 Line): $100 \times \text{Level}$
    - Double (2 Lines): $300 \times \text{Level}$
    - Triple (3 Lines): $500 \times \text{Level}$
    - Tetris (4 Lines): $800 \times \text{Level}$

- [ ] **Task 11.2: Drop Bonus Scoring**
  - Award $1$ point per cell dropped during Soft Drop.
  - Award $2$ points per cell dropped during Hard Drop.

- [ ] **Task 11.3: Level & Gravity Speed Scaling Curve**
  - Advance `Level` every 10 cleared lines.
  - Recalculate gravity timer wait time following an exponential decay speed formula (e.g., $(0.8 - (\text{Level} - 1) \times 0.007)^{\text{Level} - 1}$).

---

### Definition of Done (DoD)
This step is considered **DONE** when:
1. Clearing 1, 2, 3, or 4 lines awards the exact calculated score adjusted for the current level multiplier.
2. Soft dropping and hard dropping accumulate distance-based bonus points immediately upon execution.
3. Every 10 lines cleared increments the level count and visibly speeds up the falling speed of pieces according to the gravity curve.