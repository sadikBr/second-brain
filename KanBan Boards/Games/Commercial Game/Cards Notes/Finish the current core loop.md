---
Name: Finish the current core loop
Created At: 2026-09-10
---
- [ ]  Make `RunManager` the authoritative run-state owner: `Ready`, `Playing`, `Paused`, `Won`, `Lost`, `Results`.
- [ ] Have it emit the existing `GameEvents.RunStarted` and `RunEnded` signals.
- [ ] Stop spawning when a run ends.
- [ ] Freeze, clean up, or resolve active isotopes when the run ends.
- [ ] Add a start screen and a restart action.
- [ ] Add an end-of-run results screen.
- [ ] Add a score system.
- [ ] Award points for successful deliveries.
- [ ] Deduct score, health, or reactor stability for expired isotopes.
- [ ] Display score, run timer, reactor stability, and any combo multiplier in the HUD.
- [ ] Replace debug output (`GD.Print`) with visible game feedback.
- [ ] Give each isotope a terminal state (`Active`, `Cooling`, `Delivered`, `Vanished`) so a delivery/expiry signal cannot fire more than once.
- [ ] Ensure an isotope is no longer draggable once delivered, destroyed, or the game has ended.
- [ ] Decide whether coolant completely stops an isotope, slows it, or merely replenishes its timer—and make the behavior match the visual feedback.
- [ ] Add a short spawn grace period so a new isotope is readable before it becomes stressful.
- [ ] Add a cap on simultaneous isotopes to prevent impossible or cluttered situations.