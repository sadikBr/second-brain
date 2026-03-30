
# The Core Loop: From Void to Matter

The game will be divided into "Eras" of scientific progression.

## Phase 1: The Particle Era (The "Active" Star)

- *The Resource:* Energy and Quarks.
	
- *The Action:* You click a "Quantum Foam" in the center of the screen to generate energy.
	
- *The Crafting:* You spend energy to stabilize Quarks.
	- 3 Quarks = 1 **Proton** or **Neutron**.
	- Energy + Protons/Neutrons = **Hydrogen**.
	
- *Goal:* Reach 100 atoms of Hydrogen to unlock the **Stellar Forge**.

## Phase 2: The Atomic Era (The "Idle" Middle)

Once you have Hydrogen, the game moves from clicking to **Automation**.

- *The Periodic Table UI:* A literal periodic table where unlocked elements glow.
	
- *Fusion Mechanic:* You don't click anymore; you "Fuse."
	- H + H = He (Helium).
	- He + He = Be (Beryllium), and so on.
	
- *The Generators:* Instead of "Buildings", you buy **Scientific Equipment;**
	- *Cloud Chambers:* Automatically generates Protons.
	- *Particle Accelerators:* Multiplies the speed of Quark production.
	- *Tokamak Reactors:* Automatically performs Fusion every X seconds.

# The Strategic Twist: Stability & Decay

This is what makes the game different from Cookie Clicker.

- *Isotopes:* Sometimes, when you fuse, you get an **Unstable Isotope** (e.g. Carbon-14 instead of Carbon-12).
	
- *Radioactive Decay:* Unstable atoms eventually disappear, but they emit **Radiation (Alpha/Beta/Gamma)**.
	
- *The Trade-off:* Do you want stable atoms that stay forever, or unstable ones that decay quickly but give you a massive "Radiation Boost" to your overall production speed?

# The Prestige System: The Supernova

In every idle game, you eventually hit a "wall." In **Nuclide**, that wall is **Iron (Fe)**.

> *The Science Hook:* In real physics, fusing elements heavier than Iron _consumes_ energy rather than releasing it.

- *The Reset:* When your "Core" becomes too heavy with Iron, your star collapses. You trigger a **Supernova**.
	
- *What you lose:* All your atoms and equipment.
    
- *What you gain:* **Neutron Star Matter** (Prestige Currency).
    
- *Permanent Upgrades:* Use your Neutron Matter to buy "Fundamental Force" upgrades:
    
    - *Strong Force:* Permanent +X% to all Fusion yields.
        
    - *Weak Force:* Decreases the rate of isotope decay.
        
    - *Electromagnetism:* Increases Energy generated per click.

# Visuals & "Juice"

Since this will be an idle game, it needs to look satisfying to keep players staring at it.

- *The Centerpiece:* Instead of a cookie, I can have a **Bohr Model** (nucleus with orbiting electrons). As you unlock heavier elements, the nucleus gets bigger and more electrons start zipping around.
    
- *Color Coding:* Use the standard chemistry colors (Hydrogen is white, Oxygen is red, Nitrogen is blue).
    
- *The "Pop":* Use Godot’s `CPUParticles2D/GPUParticles2D` to create a little explosion of light every time a Fusion occurs.




# Game Prototype to see whether it is worth it.

I should start by making the game go only from **Hydrogen to Carbon**.

Try to make the loop of "Click -> Gather Quarks -> Build Proton -> Fuse Hydrogen -> Automate the process", if the game works for the first 6 elements then the rest will be just some math and UI work!