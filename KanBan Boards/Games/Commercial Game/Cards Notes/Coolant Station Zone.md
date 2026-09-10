---
Name: Coolant Station Zone
Created At: 2026-09-09
---
- **Design Objective:** Create an environmental area on the map that halts or resets a block's decay countdown.
    
- **Steps to Take:**
    
    - [x] Designate a visually distinct zone on the arena floor marked as the "Coolant Pool."
        
    - [x] Detect when any block enters the boundaries of this zone.
        
    - [x] Pause or reset the block's internal countdown timer while it remains inside the zone.
        
    - [x] Resume normal countdown behavior as soon as the block leaves the zone.
        
- **Definition of Done:** Dragging a ticking block into the Coolant Pool halts its countdown, and dragging it back out resumes its timer.