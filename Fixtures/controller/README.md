# controller

The HUD as the game draws it for a controller: the squad in a diamond bottom-left (slot 1 left,
2 top, 3 right, 4 bottom), the skill buttons in a diamond bottom-right, an "LB" badge in each.
Holding LB spreads the squad 16 px further out around a D-pad. From the owner's recordings
battle_controller.mp4, battle_controller_test1.mp4, battle_controller_test2.mp4, battle_controller_test4.mp4 battle_controller_test_fullbattle2.mp4 ("full battle 2") and battle_controller_test_lesspeople.mp4 ("fewer-operators recording") (3838x2158), UID blacked out. Kept out of the sweeps over `Fixtures/*`.

Squad: Camille, Laevatain, Si, Arcane. Values read off the frames (bar crops) and match the readers.

| File | Time | What it shows |
|---|---|---|
| `out-of-combat.jpg` | 1.5 s | Before the fight: no squad panel drawn, only the bottom-right LB badge. |
| `combat-early.jpg` | 5.0 s | Combat; slot 3 controlled; every combo ready. |
| `combat.jpg` | 10.0 s | Combat; slot 3 controlled; every combo ready; slot 3 HP ~99%. |
| `combat-combos-cooling.jpg` | 26.0 s | Slot 4's combo just used (~5%); HP 73% / 100% / 85% / 100%. |
| `combat-late.jpg` | 55.0 s | Slot 2 controlled; combos ready / ~39% / ready / ~13%; HP 77% / 100% / 72% / 100%. |
| `lb-held.jpg` | 17.0 s | LB held: squad spread around the D-pad; every combo ready. |
| `lb-held-again.jpg` | 48.2 s | LB held; combos ~86% / ready / ~82% / ready; HP 78% / 100% / 72% / 100%. |
| `three-fallen.jpg` | second recording, 221.0 s | Slots 1, 3 and 4 fallen (⊘ on a hatched square, same size as keyboard and mouse); slot 2 fighting at low HP. |
| `another-squad.jpg` | third recording, 49.5 s | Another squad: Zhuang Fangyi, Perlica, Arcane, Liino; slot 1 controlled. |
| `ultimates-two-ready.jpg` | fourth recording, 19.0 s | Ultimates (skill diamond dots): slots 1 and 3 ready (plain colour in a light ring); slot 2 ~67%, slot 4 ~47% (pale arc from 12 o'clock). |
| `ultimates-charging-one-ready.jpg` | fourth recording, 71.0 s | Ultimates ~33% / ~53% / ready / ~28%. |
| `ultimates-charging.jpg` | fourth recording, 86.0 s | Ultimates ~33% / ~60% / ~48% / ~33%. |
| `switch-keyboard-exploration.jpg` | full battle 2, 0.0 s | Exploring with keyboard and mouse (levels shown) just before the player picks up the controller for the fight: ultimates ~17% / ~71% / ready / ~72%. |
| `fullbattle-ultimates-charging.jpg` | full battle 2, 35.5 s | Controller fight: ultimates ~40% / a sliver / ~30% / ~45%. |
| `fullbattle-lb-held.jpg` | full battle 2, 71.5 s | LB held: the ultimates are large rings (not read). |
| `fullbattle-ultimate-almost-full.jpg` | full battle 2, 59.5 s | Ultimates ~65% / ~50% / ~50% / nearly full but not ready (no light ring). |
| `fullbattle-two-ready-two-almost-full.jpg` | full battle 2, 83.5 s | Ultimates ready / nearly full / ~80% / ready. |
| `two-operators.jpg` | fewer-operators recording, 179.0 s | A squad of two (Arcane left, Camille top): the right and bottom places show the empty ring with a slash; ultimates ready / ~89%. |
| `photo-mode.jpg` | 22.5 s | Photo mode: HUD hidden. |
| `target-wheel.jpg` | 31.4 s | LT held (target wheel): HUD hidden. |
| `keyboard-mouse-same-fight.jpg` | 64.0 s | The player touched the keyboard: the same fight in the keyboard-and-mouse layout. |
| `exit-dialog.jpg` | 66.0 s | The exit dialog over the keyboard-and-mouse layout. |
