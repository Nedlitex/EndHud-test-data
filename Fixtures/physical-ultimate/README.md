# physical-ultimate

Ultimate circles of Physical operators, whose ultimate is drawn in a neutral cream instead of an
element colour. One of the owner's recordings, test_mifu.mp4 (3838 × 2158, 30 fps, keyboard and
mouse): a squad of four Physical operators, Mi Fu (slot 1), Chen Qianyu, Pogranichnik and Lifeng.
Only the bottom-right 940 × 470 of each frame is kept (the ultimate circles and the battle-skill
buttons; no UID there), pasted onto a black frame of the recording's size so the readers find the
circles where they are on screen. The file name is the second the frame was taken at (`ffmpeg -ss`).

| File | What it shows (by eye, enlarged) |
|---|---|
| `mifu-60s.png` | slot 1 charging, the cream arc about a third of the way round (≈0.35); slots 2–4 ready (grey disc, white icon, light ring, key tag above) |
| `mifu-66s.png` | a white-out: the corner washed out to light grey (slot 1's centre ≈196). Slot 1 is charging, not full |
| `mifu-103s.png` | slot 1 nearly full (≈0.94) |
| `mifu-114_3s.png` | slot 1 just turned ready (enlarged ring, key tag "1"); slot 4 ready |
| `mifu-120s.png` | slot 1 empty again after the cast; slot 4 ready |

`labels.json` holds the same, per slot (1-based): `ready`, and `progress` where it is charging.

## Before the fix

`PhysicalUltimateTests` against the reader that only knew saturated element colours (commit
e0a03b4), Debug:

```
  Failed EndHud.Vision.Tests.PhysicalUltimateTests.Nearly_full_charge [190 ms]
   Assert.InRange() Failure: Value not in range
Range:  (0.84999999999999998 - 1)
Actual: 0
  Failed EndHud.Vision.Tests.PhysicalUltimateTests.Ready_right_after_filling [47 ms]
   slot 1: no reading
  Failed EndHud.Vision.Tests.PhysicalUltimateTests.Empty_again_after_the_cast [34 ms]
   slot 4: no reading
  Passed EndHud.Vision.Tests.PhysicalUltimateTests.A_white_out_is_not_a_full_charge [39 ms]
  Failed EndHud.Vision.Tests.PhysicalUltimateTests.Three_ready_and_one_about_a_third_charged [36 ms]
   slot 2: no reading
Total tests: 5
```

The charge read 0 and every ready circle gave no reading at all. The white-out test passed only
because nothing cream was read: it is there to keep the fix from reading the washed-out circle as
full.
