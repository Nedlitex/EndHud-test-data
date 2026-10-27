# Link beside the HP bar (no counter)

Crops of the owner's `test_rossi_mifu_si.mp4` (3836x2158, 30 fps): the middle of the HUD band, 540x278 px from
x 1150, y 1880 of each frame, cut the same way as `link-pulse/`. No UID in them. Tests paste each crop back at that
spot into a black 3836x2158 frame.

The controlled operator here has no counter of their own, so the game draws Link right beside the HP bar (x 1496-1571,
y 1945-2017), where Laevatain's flower or another operator's counter would otherwise be. The owner's report: "see 1:05,
[Link] is triggered, but not shown".

By eye:

| File | Time | Link |
|---|---|---|
| `link-062_75.jpg` | 62.75 s | not there (just before it appears) |
| `link-064_00.jpg` | 64.00 s | 1 (no number), at the dim end of its pulse: the sword grey, not white |
| `link-064_10.jpg` | 64.10 s | 1 (no number) |
| `link-065_00.jpg` | 65.00 s | 1 (no number), at the dim end of its pulse |
| `link-065_10.jpg` | 65.10 s | 1 (no number) |
| `link-065_50.jpg` | 65.50 s | 1 (no number) |
| `link-067_25.jpg` | 67.25 s | not there (it has ended) |

The icon pulses about once a second; 64.00 s and 65.00 s are two of its dim frames (each dip lasts a few frames,
under one reading), so one frame alone can't tell Link is there. They must not read as clearly absent.

EndHud's own gauge row is drawn above this area in the recording (its labels touch the crops' top edge); it does
not cover Link's icon.
