# Vulnerable and its stacks

Frames chosen for Vulnerable on the boss (`VulnerableRing`), from the owner's physical-team recording
`test_mifu.mp4` (3838x2158, 138 s; nothing taken from its last 5 s). Each is cut at the second in
its name (an exact frame: 30 fps, the second × 30). Everything below y 320 is blacked out (that
includes the UID): only the boss's bars, the ring and the status row are kept.

## What Vulnerable looks like

It is not in the status row. The game draws it in the infliction ring's place at the right end of
the boss's HP bar: a white shield crossed by a dark diagonal slash (lower left to upper right) on a
dark red disc, with the same white arcs as an elemental infliction around it, one per stack,
clockwise from the top: top = 1, right = 2, bottom = 3, left = 4. No digit.

When a stack is added a grey circle sweeps outwards through the arcs and an enlarged ghost of the
shield fades behind it (47.5, 49.5, 51.0, 59.5, 70.0, 94.5, 98.5 s). The same circle shows at
89.0 s and 126.0 s, the last frames before the ring went away. While the circle crosses the arcs
the count can't be told: those frames are `hard`.

## In the recording (every 0.5 s, by eye)

| Stacks | Seen |
|---|---|
| 1 | 47.5–49.0, 59.5–63.5, 66.0, 94.5–98.0 s |
| 2 | 49.5–50.5, 69.0–69.5, 99.0–103.0 s |
| 3 | 51.0–54.0, 55.0, 70.5–71.5, 103.5–115.0 s |
| 4 | 72.0–76.0, 78.5, 81.5–89.5, 118.0–126.0 s |

The ring is not there 0–47.0 s (exploring, then the fight starts), and it comes and goes inside the
fight: gone at 54.5, 55.5–59.0, 64.0–65.5, 66.5–68.5, 76.5–78.0, 79.0–81.0, 90.0–94.0 and from
126.5 s. Some of those gaps are the whole top HUD hidden or dark (an ultimate, a dark scene); in
others the HP bar's ends are still drawn and the ring is not. Why it went each time (consumed by a
skill, expired, or the HUD hidden) can't be told from the picture and isn't labelled.

At 81.5 s the HUD fades back in: the arcs and shield are grey, not white (`dim-4-81_5s.jpg`).

## Files

`labels.json`: `vulnerable` (the shield is shown), `stacks` (1–4 by eye, `null` when it can't be told
or there is no ring), `hard` (a flash, a beam or a dim HUD over the ring: the count may read as
unknown, never as another number; presence must still be read).

| File | Shows |
|---|---|
| `vulnerable-1-48s.jpg` | 1 stack, a cyan beam across the ring's lower left (`hard`) |
| `vulnerable-1-61s.jpg`, `vulnerable-1-96s.jpg` | 1 stack |
| `vulnerable-1-66s.jpg` | 1 stack over a white scene |
| `vulnerable-2-50s.jpg`, `-69s`, `-100s`, `-103s` | 2 stacks |
| `vulnerable-3-52s.jpg`, `-71s`, `-104_5s`, `-110s` | 3 stacks |
| `vulnerable-3-55s.jpg` | 3 stacks, a faint ghost shield behind |
| `vulnerable-4-74s.jpg`, `-85s`, `-122s` | 4 stacks |
| `flash-1-47_5s.jpg` | the ring appearing (1 stack), the circle on the arcs (`hard`) |
| `flash-2-49_5s.jpg` | 1 → 2, the circle outside the arcs (`hard`) |
| `flash-3-51s.jpg` | 2 → 3, the circle near the arcs: read as 4 unless the gaps are checked (`hard`) |
| `flash-98_5s.jpg` | 1 → 2, the circle on the arcs; only the top arc can be told (`hard`, stacks `null`) |
| `flash-4-89s.jpg`, `flash-4-126s.jpg` | 4 stacks, the circle, just before the ring went (`hard`) |
| `dim-4-81_5s.jpg` | 4 stacks, the HUD fading back in, grey (`hard`) |
| `gone-54_5s.jpg` | no ring, between two frames with 3 stacks |
| `none-56s.jpg`, `none-92s.jpg`, `none-117_5s.jpg` | no ring |
| `none-white-35s.jpg` | no ring, a white wall behind its place |
| `none-typhoeus-edge-27s.jpg` | from `typho_battle.mp4` at 27 s (an arts team, no Vulnerable): no ring, grey sky over a dark roof edge, the closest any frame of four arts-team recordings came to a white shield with a dark line through it |

No elemental infliction shows in this recording, so whether the ring can hold an infliction and
Vulnerable at once, or which one wins, is not known.
