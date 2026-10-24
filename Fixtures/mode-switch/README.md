# mode-switch

The mode switch at the top left (探索 exploring / 工业 building, `ModePill`): drawn in the open world
only. While it shows with its plain icon the player is out of battle and the battle HUD stays down;
its icon turns red while a fight is on in the open world (see `controller/ultimates-charging*.jpg`).
An instance's battle draws the evacuate bar (撤离) there instead (every `combat-*`/`battle-*` fixture).
Kept out of the sweeps over `Fixtures/*`. UID blacked out.

| File | Source | What it shows |
|---|---|---|
| `controller-exploring.jpg` | battle_controller_test4.mp4, 12.0 s (3838x2158) | Controller layout, exploring: the switch on 探索 with the D-pad arrow on its left (no fight yet); levels under the portraits. |
| `controller-exploring-bright-sky.jpg` | battle_controller_test4.mp4, 56.5 s | Exploring after a fight, a bright sky above and below the switch's dark band (the switch scored 0.81 while the sky was compared too). |
| `controller-fight-bright-sky.jpg` | battle_controller_test4.mp4, 23.0 s | A fight in the open world: the switch's icon red, a bright sky around it (0.82 while the sky was compared). |
| `controller-evacuate-bar.jpg` | battle_controller_test_fullbattle2.mp4, 49.5 s | An instance's battle: the evacuate bar (撤离) where the switch would be, the highest it scored in the recordings checked (0.77). |
| `keyboard-building.jpg` | The owner's screenshot, 2026-10-24 (3840x2160) | Keyboard and mouse, building: the switch on 工业, the white slider over the lightning bolt instead of the compass; the factory toolbar at the bottom, no squad panel. |
