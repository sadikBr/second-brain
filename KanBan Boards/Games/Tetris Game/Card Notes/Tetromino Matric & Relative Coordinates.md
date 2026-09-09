---
Name: Tetromino Matric & Relative Coordinates
Created At: 2026-09-06
Due Date:
---
# Tetromino Matrix & Relative Coordinates

- [ ] **Task 2.1: Local Vector Grid Mapping**
  - Define all 7 standard shapes ($I, J, L, O, S, T, Z$) as relative coordinate arrays centered around a local origin $(0, 0)$.
  - Standardize initial orientations so shapes spawn horizontally centered with their flat side facing down.

- [ ] **Task 2.2: Color & Type Identifiers**
  - Assign distinct shape IDs and color metadata to each shape structure.
  - Store metadata immutably so both active pieces and frozen playfield blocks draw from a unified color mapping.

- [ ] **Task 2.3: Bounding Box Definitions**
  - Map $3 \times 3$ bounding boxes for $J, L, S, T, Z$ pieces around pivot $(1, 1)$.
  - Map a $4 \times 4$ bounding box for the $I$-piece around pivot $(1.5, 1.5)$.
  - Map a fixed $2 \times 2$ matrix for the $O$-piece (no rotation required).

---

### Definition of Done (DoD)
This step is considered **DONE** when:
1. All 7 shapes can be instantiated programmatically, rendering their correct geometry via local offsets.
2. Every shape displays its official guideline color tint correctly.
3. Querying any piece returns its exact immutable matrix bounds and default spawn offset without runtime allocation errors.