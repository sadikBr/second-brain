---
Name: Event-Driven HUD, Overlays & Sound
Created At: 2026-09-06
Due Date:
---
# Step 12: Event-Driven HUD, Overlays & Sound

- [ ] **Task 12.1: Signal & Observer Binding**
  - Connect game events to UI display nodes via decoupled signals:
    - `score_updated(new_score)` $\to$ updates score label.
    - `level_updated(new_level)` $\to$ updates level label.
    - `lines_updated(total_lines)` $\to$ updates lines label.
    - `queue_updated(queue_array)` $\to$ updates next-piece preview panel.
    - `hold_updated(shape_type)` $\to$ updates hold-piece panel.

- [ ] **Task 12.2: Game Over & Pause Overlays**
  - Create modal overlay screens for pause states and game-over screens containing score breakdowns and retry buttons.

- [ ] **Task 12.3: Audio Feedback Integration**
  - Wire sound effects to game events: move tick, rotation click, soft drop, hard drop impact, line clear chime, game over event, and background music loop.

---

### Definition of Done (DoD)
This step is considered **DONE** when:
1. All HUD panels (Score, Level, Lines, Next Queue, Hold Display) update instantly in response to game signals without direct polling.
2. Triggering a Game Over displays a modal with final stats and a functioning restart trigger that resets the board state cleanly.
3. Audio clips play reliably in sync with user inputs, line clear triggers, and state transitions without clipping or latency.