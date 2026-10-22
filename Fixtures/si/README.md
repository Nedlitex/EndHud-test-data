# Si

Single frames from a recording of the owner's own boss fight at 4K (3838 × 2158, 30 fps), Si
controlled in squad slot 1, keyboard and mouse. The file name is the second the frame was taken at
(none from the recording's last 5 s). Everything is blacked out except the two regions read: the
bottom centre (x 1380–2460, y 1880–2158: the HP bar and what sits left of it) and the bottom right
(x 2860–3838, y 1680–2158: the ultimate circles and battle-skill buttons). That also blacks out the
UID. `labels.json` gives, by eye, what the readers must say.

## `stacks-*.jpg`: Si's damage stacks (伤害层数)

Left of the HP bar, where Laevatain draws her 熔火 flower. `stacks`:

- `0`: a hollow green four-lobed flower with no number (`14s`, `38_5s`, `65_5s`, `97_75s`: right
  after each cast of her battle skill, which spends the stacks).
- `1` and up: a green cross with a white number, one or two digits (up to 45 here; the game sets no
  maximum). Every digit 0–9 is in at least two frames. Some are on bright backgrounds (`22_25s`,
  `46_75s`, `50_75s`, `61_75s`).
- `null`: no badge to read: the cast flash (`36_5s`, `64_5s`), a white screen (`43_25s`, `80_75s`,
  `113_25s`), an effect over the HUD (`44s`).

## `skill-*.jpg`: her battle-skill button (slot 1)

From the first use, the button's icon changes from a butterfly to a swirl, and a light-grey ring
inside the button drains clockwise from 12 o'clock while the skill lasts; the butterfly comes back
when it ends. `icon` is `Original` (butterfly) or `Changed` (swirl). On swirl frames
`drainedDegrees` is how much of the ring is gone, by eye on an enlarged crop (±10°), and
`secondsLeft` = 22 × (1 − drained / 360) (the ring takes about 22 s: full at 13.5 s, gone at
35.5 s, butterfly back at 35.75 s).

- `10_5s`, `12s`: before the first cast (butterfly; dimmed at `10_5s`).
- `13_5s` to `35_25s`: the first cast running. `ringHidden` at `19_5s` and `20s`: the whole button
  fades for a moment and the ring can't be told from the background.
- `35_75s`, `36s`: it ended (butterfly again).
- `37s` to `40_5s`: the second cast (a full ring again at `37s`).
