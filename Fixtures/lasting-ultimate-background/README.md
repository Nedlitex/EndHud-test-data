# lasting-ultimate-background

Whose lasting ultimate the time bar shows (the thin line right above the skill points, read by
`UltimateTimeBar`) when the operator it belongs to is NOT the one controlled. Whole frames from
two of the owner's recordings, 3838 × 2158, keyboard and mouse, UID blacked out (bottom left);
none from a recording's last 5 s. The file name is the clip and the second (`ffmpeg -ss`).

The owner was running an older EndHud while recording: its gauges are drawn bottom centre, above
the HP bar (the circles labelled 终结技 / 青霆剑 / 熔火 / 持续中). They are EndHud's own drawing,
not the game's, and show the bug being fixed: 持续中 on the controlled operator's circle.

## `zh-`: test_zhuang_background1.mp4

Squad: Zhuang Fangyi (slot 1), Perlica (slot 2), Arcane, Liino. Perlica is controlled the whole
time. Zhuang's ultimate is cast from the background at about 36 s (cutscene 35.75–38 s; her
ultimate circle, bottom right, reads ready until 38.25 s and empty from 38.5 s). From 38.25 s the
gold bar runs under Perlica's HP, full, draining to about 0.11 at 69.5 s; Zhuang is never
controlled.

| File | What it shows |
|---|---|
| `zh-34s.jpg` | before: no bar, every ultimate ready |
| `zh-38_5s.jpg` | the gold bar full, Perlica controlled |
| `zh-46_5s.jpg`, `zh-52s.jpg`, `zh-63s.jpg` | the gold bar draining (≈0.73, 0.5, 0.37), Perlica controlled |

## `zl-`: test_zhuang_laevatine_background1.mp4

A squad of three: Zhuang Fangyi (slot 1), Laevatain (slot 2) and Yvonne (slot 3; named by
the owner, 2026-10-23). All three cast their ultimate, and each lasts with the bar: Zhuang's runs
from about 36 s, Laevatain's from 38.75 s (a full red bar under her), Yvonne's (a teal bar) from 41.25 s (her ultimate's
cutscene is 39.25–41 s; her bar reads 1.00 at 41.25 s and 0.57 at 44.25 s, draining about 0.14 a
second, so about 7 s in all; it isn't on screen again before it would have ended). The player
switches between all three. What the bar shows depends on who is controlled:

| File | Controlled | The bar |
|---|---|---|
| `zl-36_5s.jpg` | slot 1, Zhuang | gold, full: Zhuang's |
| `zl-43_5s.jpg` | slot 2, Laevatain | red ≈0.83: Laevatain's (Zhuang's still runs) |
| `zl-44_5s.jpg` | slot 3, Yvonne | teal ≈0.54: Yvonne's |
| `zl-46s.jpg` | slot 1, Zhuang | gold ≈0.78: Zhuang's |
| `zl-53_5s.jpg` | slot 2, Laevatain | red ≈0.15: Laevatain's |
| `zl-56s.jpg` | slot 3, Yvonne | gold ≈0.38: Zhuang's, running in the background (Yvonne's has ended) |

So: the bar shows the controlled operator's own lasting ultimate when she has one running, and
otherwise one that runs for an operator in the background, in that operator's colour. It is not
"the controlled operator's" bar.

## `labels.json`

By eye. `controlledSlot`: the slot with the large portrait. `bar`: the bar's colour, null when
there is none. `owner`: whose ultimate it is (operator id), null when there is no bar.
