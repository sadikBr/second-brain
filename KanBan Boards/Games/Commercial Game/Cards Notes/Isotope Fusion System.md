---
Name: Isotope Fusion System
Created At: 2026-09-09
---
- **Design Objective:** Allow identical blocks to combine into a single, higher-value block upon collision.
    
- **Steps to Take:**
    
    - [ ] Detect physical contact between two blocks.
        
    - [ ] Compare the tier level of both colliding blocks.
        
    - [ ] If the tiers match, remove both blocks and create a single higher-tier block in their place with a fresh timer.
        
    - [ ] If the tiers do not match, allow them to bounce off each other normally.
        
- **Definition of Done:** Colliding two identical Tier-1 blocks merges them into a single Tier-2 block, while colliding mismatched blocks simply bounces them apart.