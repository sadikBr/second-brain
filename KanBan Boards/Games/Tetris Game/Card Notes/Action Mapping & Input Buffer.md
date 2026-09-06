---
Name: Action Mapping & Input Buffer
Created At: 2026-09-06
Due Date:
---
# Step 3: Action Mapping & Input Buffer

- [ ] **Task 3.1: Input Action Schema**
  - Register discrete input triggers: `move_left`, `move_right`, `soft_drop`, `hard_drop`, `rotate_cw`, `rotate_ccw`, `hold_piece`.

- [ ] **Task 3.2: DAS (Delayed Auto-Shift) Architecture**
  - Design a dual-timer input buffer for lateral movement:
    - Initial delay timer (e.g., $160\text{ms}$) before continuous sliding activates.
    - Auto-repeat rate timer (e.g., $30\text{ms}$) for rapid grid sliding once DAS is primed.

- [ ] **Task 3.3: Input Interruption & Priority Rules**
  - Cancel active DAS direction immediately when the opposing directional key is pressed.
  - Ensure instant single-frame execution for `hard_drop` and `hold_piece`, bypassing the DAS buffer entirely.

---

### Definition of Done (DoD)
This step is considered **DONE** when:
1. Pressing a directional key once moves the target by exactly one grid cell.
2. Holding a directional key causes a precise initial delay (DAS) before smoothly repeating movement at the configured rate.
3. Opposing inputs immediately override active sliding without getting stuck in contradictory states.