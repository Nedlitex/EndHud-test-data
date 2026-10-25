# Battle-skill cast flash

The bottom-right 820×370 px of single 4K frames (3838×2158 recordings, so the game's HUD at scale
0.999): the four battle-skill buttons and the bottom of the ultimate circles above them. Nothing
else is in the crop (the UID is bottom left). Used by `BattleSkillFlashTests`.

When an operator casts a battle skill, the dark top half of that slot's button turns flat light
grey for 2–10 frames at 30 fps, then a white ring grows out of the button. An empowered battle
skill draws a thick white ring on the button's rim that stays for seconds instead.

| File | Recording, frame | What the frame shows |
|---|---|---|
| `bug1-rest.png` | test_battle_track_bug1, 25.10 s | Every button at rest (no flash) |
| `bug1-slot3-fill-starting.png` | test_battle_track_bug1, 25.90 s | Slot 3's fill just starting (not yet light) |
| `bug1-slot3-fill.png` | test_battle_track_bug1, 25.93 s | Slot 3 casts: its button's top half filled light grey |
| `bug1-scene-light.png` | test_battle_track_bug1, 23.93 s | A pink and white burst of the scene behind slots 2–4 (no cast) |
| `fullbattletest-slot2-fill.png` | fullbattletest, 24.05 s | Slot 2 casts: the fill |
| `fullbattletest-slot2-countdown.png` | fullbattletest, 24.12 s | Slot 2 right after: dark disc with its countdown (60) |
| `fullbattletest-slot2-empowered-start-fill.png` | fullbattletest, 79.13 s | Slot 2's empowered glow starting: a fill, rim not lit yet |
| `fullbattletest-slot2-empowered-rim.png` | fullbattletest, 79.77 s | Slot 2 empowered: the white rim lit, the disc not filled |
| `fullbattletest-slot2-empowered-cast-fill.png` | fullbattletest, 79.83 s | Slot 2 casts while empowered: a fill inside the lit rim |
| `typho-slot1-purple-fill.png` | typho_battle, 53.73 s | Slot 1 casts in front of a purple scene that tints the fill |

Cut with ffmpeg (`crop=820:370:iw-820:ih-370`, one frame, metadata stripped), each frame chosen by
measuring the button, from the maintainer's own recordings, none from a recording's last 5 s.

## Controller

The bottom-right 710×680 px of single frames of battle_controller_test_fullbattle3 (3838×2158, a
controller fight; Laevatain in slot 2, see `Fixtures/controller`): the skill diamond, plain (an "LB"
badge in the middle) and with LB held (a larger diamond up and to the left, a face-button badge X, Y,
B, A beside each button). A battle skill is cast with LB held, so its flash is in the held diamond:
the pressed button turns light grey, then white. Nothing else is in the crop (the UID is bottom left).
Cut with `crop=710:680:iw-710:ih-680`, one frame, metadata stripped. Used by `BattleSkillFlashTests`.

| File | Time | What the frame shows |
|---|---|---|
| `controller-rest.png` | 30.00 s | The plain diamond, every button at rest |
| `controller-held-slot3-pressed.png` | 26.90 s | LB held, slot 3 (B) pressed: light grey, before its flash |
| `controller-held-slot3-fill.png` | 27.00 s | LB held, slot 3 casts: its button white |
| `controller-held-slot1-fill.png` | 27.90 s | LB held, slot 1 (X) casts: its button white |
| `controller-held-slot3-fill-slot2-empowered.png` | 79.33 s | LB held, slot 3 casts in front of a light floor, while slot 2's rim glows (empowered) |
| `controller-held-slot1-empowered.png` | 99.70 s | LB held, slot 1's rim glows (empowered), no cast |
| `controller-slot1-empowered.png` | 93.50 s | The plain diamond, slot 1's rim glows (empowered) |
| `controller-slot2-empowered.png` | 123.00 s | The plain diamond, slot 2's rim glows (empowered) |
| `controller-scene-light.png` | 80.60 s | A white beam of the scene behind the see-through buttons: every rim lit, no glow |
| `controller-held-slot1-ultimate-press.png` | 146.90 s | LB held, slot 1 held down for its ultimate (the cutscene follows): white like a cast |

## Samples

`samples/` holds the four buttons measured on every frame (30 fps) of a few seconds of the same
recordings, one line per frame: the time in seconds, then per button (slot 1 first, separated by
`|`) the fill, its spread, the scene round the button and the rim's white share, as
`BattleSkillFlash` defines them (measured with the research script that set its thresholds). Used
by `CastFlashTrackerTests`.

| File | Recording, seconds | What happens |
|---|---|---|
| `bug1-slot3-cast.txt` | test_battle_track_bug1, 25.4–26.8 | Slot 3 casts at 25.93 (no cooldown) |
| `bug1-scene-light.txt` | test_battle_track_bug1, 23.4–24.9 | Scene light behind slots 2–4 for about 0.6 s, no cast |
| `fullbattletest-slot2-cast-countdown.txt` | fullbattletest, 23.5–24.9 | Slot 2 casts at 24.03 and goes dark with its countdown |
| `fullbattletest-slot2-empowered.txt` | fullbattletest, 78.5–80.7 | Slot 2's empowered glow starts at 79.13; the empowered cast at 79.80 ends it |
