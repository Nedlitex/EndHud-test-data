# Vulnerable and an elemental infliction at once

Frames chosen for the boss carrying Vulnerable and an elemental infliction together
(`InflictionRing`, `VulnerableRing`, `BossStatusReader`), from the owner's recording
`test_rossi.mp4` (3838x2158, 30 fps, 44.4 s; nothing taken from its last 5 s). Each is cut at the
second in its name (an exact frame: the second × 30). Everything below y 320 is blacked out (that
includes the UID): only the boss's bars, the icons beside them and the status row are kept.

## How two show

The game draws both, side by side, at the right end of the boss's HP bar:

- the first stays in the ring's old place (`InflictionRing.Area`, centre (2480, 142) at 4K);
- the second is the same size, 94 px (4K) to its right, at the same height;
- the order is the order they were applied: heat first then Vulnerable at 20-25 s, Vulnerable
  first then heat (33 s) or cryo (37 s) later on;
- each has its own white stack arcs, clockwise from the top (top = 1, right = 2, bottom = 3,
  left = 4), as when it is alone;
- when the first goes, it fades in place for a moment (25.5 s: the heat icon grey, Vulnerable still
  second), then the second moves into the first place (25.75 s).

Measured with the ring readers at an offset: the shield's white share and slash, and the heat icon's
coloured share, peak at 93-95 px right of the first ring's centre on both 23 s (heat, Vulnerable)
and 33 s (Vulnerable, heat).

## In the recording (every 0.25 s, by eye and the ring readers)

| Seconds | First | Second |
|---|---|---|
| 0-15.25 | none (exploring, then the fight starts) | none |
| 15.5-16.75 | heat 1 | none |
| 17.0-19.75 | heat 2 | none |
| 20.0-24.75 | heat 2 | Vulnerable 1 (20.0: arriving, a circle round it) |
| 25.0 | heat 2, a circle | Vulnerable, a circle (count can't be told) |
| 25.25 | heat 2 | Vulnerable 3, a ghost shield behind |
| 25.5 | heat, fading grey | Vulnerable 3 |
| 25.75-32.5 | Vulnerable 3 | none |
| 32.75-36.0 | Vulnerable 3 | heat 1 (32.75: arriving, a circle) |
| 36.25-36.5 | Vulnerable 3 | none |
| 36.75-37.75 | Vulnerable 3 | cryo 1 (36.75-37.0: arriving, a circle) |
| 38.0-39.25 | none (the HUD gone, another scene) | none |

At 22.75 s the heat icon's colour dims for a frame and it reads as unknown.

## Files

`labels.json`: per file, `first` and `second` (the icon in the first place and the one to its
right, `null` when there is none), each with `status` (the wiki's id), `stacks` (by eye; `null` when
it can't be told) and `hard` (a circle, a ghost or a fade over that icon: it may be read with an
unknown count, or not at all, never as another status or count).

| File | Shows |
|---|---|
| `heat-2-vulnerable-1-21s.jpg`, `-22_8s`, `-23_5s`, `-24_5s` | heat 2, then Vulnerable 1 |
| `heat-2-vulnerable-3-25_3s.jpg` | heat 2, then Vulnerable 3 with a ghost shield (both `hard`) |
| `vulnerable-3-heat-1-33_5s.jpg`, `-35s` | Vulnerable 3, then heat 1 |
| `vulnerable-3-cryo-1-37_5s.jpg` | Vulnerable 3, then cryo 1 |
| `heat-1-16s.jpg`, `heat-2-18_5s.jpg` | heat alone, 1 and 2 stacks |
| `vulnerable-3-28s.jpg`, `-30s` | Vulnerable 3 alone |
| `arriving-vulnerable-20s.jpg` | heat 2; Vulnerable 1 arriving second, a circle round it (`hard`) |
| `flash-heat-2-vulnerable-25s.jpg` | circles over both: heat 2, Vulnerable (count can't be told) (`hard`) |
| `fading-heat-vulnerable-3-25_5s.jpg` | heat fading grey in the first place, Vulnerable 3 still second (`hard`) |
| `moved-vulnerable-3-25_8s.jpg` | Vulnerable 3 moved into the first place, a yellow effect behind |
| `arriving-heat-32_8s.jpg` | Vulnerable 3; heat 1 arriving second, a circle round it (`hard`) |
| `gone-heat-vulnerable-3-36_5s.jpg` | heat gone, Vulnerable 3 alone |
| `arriving-cryo-37s.jpg` | Vulnerable 3; cryo 1 arriving second, a circle round it (`hard`) |
| `none-10s.jpg`, `none-39s.jpg` | no icon (exploring; the HUD gone) |
