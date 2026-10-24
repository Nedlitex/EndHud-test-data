# mode-switch

The mode switch at the top left (探索 exploring / 工业 building, `ModePill`): drawn in the open world
only. While it shows with its plain icon the player is out of battle and the battle HUD stays down;
its icon turns red while a fight is on in the open world (see `controller/ultimates-charging*.jpg`).
An instance's battle draws the evacuate bar (撤离) there instead (every `combat-*`/`battle-*` fixture).
Kept out of the sweeps over `Fixtures/*`. UID blacked out.

| File | Source | What it shows |
|---|---|---|
| `controller-exploring.jpg` | battle_controller_test4.mp4, 12.0 s (3838x2158) | Controller layout, exploring: the switch on 探索 with the D-pad arrow on its left (no fight yet); levels under the portraits. |
| `keyboard-building.jpg` | The owner's screenshot, 2026-10-24 (3840x2160) | Keyboard and mouse, building: the switch on 工业, the white slider over the lightning bolt instead of the compass; the factory toolbar at the bottom, no squad panel. |
