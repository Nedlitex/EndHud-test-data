# si-timer-second-cast

Si's battle-skill button through a SECOND cast of the skill while it still lasts. Whole frames
from two of the owner's recordings, keyboard and mouse, UID blacked out (bottom left); none from
a recording's last 5 s. The file name is the clip and the second the frame was taken at
(`ffmpeg -ss`).

| Prefix | Recording | Size | Si's place | Button read |
|---|---|---|---|---|
| `lae-` | test_laevatine_background1.mp4 | 3838 × 2158 | slot 3 of 4 | 2 (0 = leftmost) |
| `si-` | test_si_background1.mp4 | 3838 × 2154 | slot 1 of 4 | 0 |

## What the button shows

1. Before: the butterfly (`Original`).
2. The first cast: the swirl in a diamond (`Changed`), and the grey ring inside the button,
   full, starts draining clockwise from 12 o'clock.
3. The second cast, while the swirl is up: the icon becomes a butterfly crossed out inside a
   ring with four points (`SecondCast`). The ring does NOT fill again: it goes on draining from
   where it was (`lae-` 23.5 s swirl at 20° drained, 24 s crossed at 25°; `si-` 48.5 s swirl at
   275°, 49.5 s crossed at 290°).
4. The ring empties while the crossed icon is still up (`lae-37s`, `si-63s`), and about half a
   second later the butterfly is back (`lae-37_5s`, dimmed: not enough skill points;
   `si-63_5s`).

So the skill lasts from the first change of the icon until the butterfly returns, the second
cast included, and the ring is one clock for the whole of it.

Seen in the measurements behind these frames (every 0.25 s, the reader's ring):

- The ring stands still while the game is paused for a cutscene: `si-` 51–60 s (another
  operator's ultimate) it went from 0.146 to 0.104 only. The first cast took 31.25 s → 63 s
  of the recording.
- In `lae-` the ring went from 0.42 left (36.75 s) to empty (37 s) at once, and the butterfly
  came back at 37.5 s: the skill ended before the ring ran out. Why is not known.

## `labels.json`

By eye on enlarged crops of the button. `icon` as above; `hidden` where the button can't be
seen at all (a cutscene, a white flash). `drainedDegrees`: how much of the ring is gone,
clockwise from 12 o'clock, from the reader's value checked by eye on the crop (agrees within
±10°); 360 = the ring is gone.
