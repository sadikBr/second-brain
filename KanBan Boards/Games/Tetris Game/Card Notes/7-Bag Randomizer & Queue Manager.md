---
Name: 7-Bag Randomizer & Queue Manager
Created At: 2026-09-06
Due Date:
---
# Step 9: 7-Bag Randomizer & Queue Manager

- [ ] **Task 9.1: Fisher-Yates Shuffle Generator**
  - Implement a bag randomizer class containing one instance of each of the 7 shapes.
  - Shuffle array using Fisher-Yates algorithm whenever the bag empties to prevent drought or flood of specific shapes.

- [ ] **Task 9.2: Multi-Piece Queue Buffer**
  - Maintain a preview buffer holding upcoming pieces (typically 3 to 5 shapes ahead).
  - Expose a `pop_next()` method that serves the front shape and automatically tops off the queue buffer from the bag generator.

- [ ] **Task 9.3: Peek Inspection Data API**
  - Expose a read-only query method allowing the HUD preview panels to inspect upcoming queued shapes without modifying the queue state.

---

### Definition of Done (DoD)
This step is considered **DONE** when:
1. Generating 70 consecutive pieces guarantees that every 7-piece sequence contains exactly one instance of each shape ($I, J, L, O, S, T, Z$).
2. The preview queue maintains a constant buffer of upcoming shapes that match the exact sequence popped onto the board.
3. No shape is starved for more than 12 drops.