---
Name: Match Loop & Victory Loss Conditions
Created At: 2026-09-09
Due Date:
---
- **Design Objective:** Track total shift progress and resolve the game round with a win or loss state.
    
- **Steps to Take:**
    
    - [ ] Create an interface tracking three values: Shift Time Remaining, Current Quota Progress, and Facility Meltdown Level.
        
    - [ ] Increase Quota Progress whenever points are scored at the Delivery Chute.
        
    - [ ] Increase Meltdown Level whenever a block explodes.
        
    - [ ] Trigger a "Shift Win" outcome if the Quota Target is reached before time runs out.
        
    - [ ] Trigger a "Facility Meltdown" outcome if Meltdown reaches 100% or if time expires before meeting the Quota.
        
- **Definition of Done:** You can play a full match from start to finish where filling the score quota shows a victory screen, and allowing too many explosions shows a defeat screen.