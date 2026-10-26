# Link pulsing over a light floor

Crops of the owner's `test_battle_debug.mp4` (3838x2158, 30 fps): the middle of the HUD band, 540x278 px from
x 1150, y 1880 of each frame (the controlled operator's HP bar, Link's icon left of it, Laevatain's counter). No UID
in them. Tests paste each crop back at that spot into a black 3838x2158 frame.

By eye: Link (one stack, no number) is shown in every one of them, all the way from 81.8 s to the end of the
stretch. The owner's report: "look at 1:24 - 1:35, the [Link] buff is flashing and even gone, but the actual buff is
always there".

What makes it hard to read: the icon pulses about once a second (its sword dims to grey and back), and here it is
over a light grey floor, so at the dim end of the pulse it matches only just under the reader's bar; a white sky
band and a red beam pass behind it (86.0 s, 86.5 s), light effects over it (87.5 s, 91.1-91.5 s), and the HUD jolts
and dims (83.8 s).

| Folder | What | Times |
|---|---|---|
| `readings/` | four readings a second, as the app reads | 82.25 s to 95.75 s, `link-SSS_hh.jpg` = SSS.hh s |
| `frames/` | every frame of the worst stretches | 87.400-88.067 s, 91.100-91.500 s, 94.600-95.300 s, `link-SSS_mmm.jpg` |

EndHud's own gauge row is drawn above this area in the recording (its labels touch the crops' top edge); it does
not cover Link's icon.
