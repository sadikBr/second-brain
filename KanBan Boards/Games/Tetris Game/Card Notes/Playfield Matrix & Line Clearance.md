---
Name: Playfield Matrix & Line Clearance
Created At: 2026-09-06
Due Date:
---
# Step 8: Playfield Matrix & Line Clearance

- [ ] **Task 8.1: 2D Spatial Array Structure**
  - Maintain a $10 \text{ columns} \times 20 \text{ rows}$ matrix storing block node references or `null` for empty space.

- [ ] **Task 8.2: Full Row Evaluation**
  - Scan rows bottom-to-top ($Y = 19 \to 0$) after a piece locks.
  - Identify a full row when all 10 column indices contain non-null block references.

- [ ] **Task 8.3: Line Clearing & Matrix Collapse**
  - Clear full row memory entries and free corresponding block instances.
  - Shift all stored block references in rows above down by $+1$ array index.
  - Update physical visual positions of shifted blocks to reflect new matrix indices.

---

### Definition of Done (DoD)
This step is considered **DONE** when:
1. Completing a horizontal line of 10 blocks instantly clears those block references from memory and destroys their visual nodes.
2. All block rows floating above a cleared line drop down by the exact number of cleared rows.
3. Clearing multiple non-consecutive or simultaneous rows (e.g., a 4-row Tetris) updates the grid array accurately without leaving floating or corrupt references.