---
Name: Rotational Transformations & Offset Math
Created At: 2026-09-06
Due Date:
---
# Rotational Transformations & Offset Math

- [ ] **Task 4.1: Rotational State Indices**
  - Define 4 rotational states per shape: $0$ (Spawn), $1$ ($90^\circ$ Clockwise), $2$ ($180^\circ$), $3$ ($270^\circ$ Counter-Clockwise).

- [ ] **Task 4.2: Transformation Matrix Algorithms**
  - Implement Clockwise vector transformation: $(x, y) \to (-y, x)$.
  - Implement Counter-Clockwise vector transformation: $(x, y) \to (y, -x)$.

- [ ] **Task 4.3: Local-to-World Vector Mapping**
  - Write a translation algorithm that combines an active piece's global `GridPosition` with its transformed local block offsets to output absolute playfield grid coordinates.

---

### Definition of Done (DoD)
This step is considered **DONE** when:
1. A 360-degree clockwise rotation sequence ($0 \to 1 \to 2 \to 3 \to 0$) returns all blocks to their exact starting offsets.
2. Counter-clockwise transformations mirror clockwise operations symmetrically across all shapes.
3. The translation function correctly maps local matrix coordinates to absolute integer positions on the $10 \times 20$ grid.