# physical-ultimate

Ultimate circles of Physical operators, whose ultimate is drawn in a neutral cream instead of an
element colour. Two of the owner's recordings, keyboard and mouse. Only the bottom-right 940 × 470
of each frame is kept (the ultimate circles and the battle-skill buttons; no UID there), pasted
onto a black frame of the recording's size so the readers find the circles where they are on
screen. The file name is the clip and the second the frame was taken at (`ffmpeg -ss`).

| Prefix | Recording | Size | Squad |
|---|---|---|---|
| `mifu-` | test_mifu.mp4 | 3838 × 2158 | four Physical operators: Mi Fu (slot 1), Chen Qianyu, Pogranichnik, Lifeng |
| `rms-` | test_rossi_mifu_si.mp4 | 3836 × 2158 | Rossi (slot 1, red), Si (slot 2, cyan), Camille (slot 3, red), Mi Fu (slot 4, cream) |

| File | What it shows (by eye, enlarged) |
|---|---|
| `mifu-60s.png` | slot 1 charging, the cream arc about a third of the way round (≈0.35); slots 2–4 ready (grey disc, white icon, light ring, key tag above) |
| `mifu-66s.png` | a white-out: the corner washed out to light grey (slot 1's centre ≈196). Slot 1 is charging, not full |
| `mifu-103s.png` | slot 1 nearly full (≈0.94) |
| `mifu-114_3s.png` | slot 1 just turned ready (enlarged ring, key tag "1"); slot 4 ready |
| `mifu-120s.png` | slot 1 empty again after the cast; slot 4 ready |
| `rms-94s.png` | slot 4 charging (≈0.93) under a pale cyan figure from another operator's ultimate, which lights the disc and the ring round it. Not ready |
| `rms-100s.png` | slot 4 nearly full (≈0.96); slot 1 red, ready (key tag "1") |
| `rms-111_5s.png` | slot 4 empty after its cast; slot 2 cyan ≈0.3 |
| `rms-107_5s.png` | slot 4 ready (key tag "4"); slot 2 cyan ≈0.3, slot 3 red ≈0.5, slot 1 empty |
| `rms-140s.png` | slot 4 charging ≈0.18, over a light floor (its empty centre is a lighter grey, ≈98) |

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

The `rms-` frames came after that first fix, which accepted a grey ready disc on the icon test
the coloured circles use (white share >= 0.08). Against it (Debug):

```
[xUnit.net 00:00:00.71]       slot 4 read as ready
  Passed EndHud.Vision.Tests.PhysicalUltimateTests.Nearly_full_charge [55 ms]
  Passed EndHud.Vision.Tests.PhysicalUltimateTests.Ready_right_after_filling [27 ms]
  Passed EndHud.Vision.Tests.PhysicalUltimateTests.Charging_over_a_light_floor [27 ms]
  Failed EndHud.Vision.Tests.PhysicalUltimateTests.A_light_effect_over_a_charging_circle_is_not_ready [28 ms]
   slot 4 read as ready
  Passed EndHud.Vision.Tests.PhysicalUltimateTests.Empty_again_after_the_cast [20 ms]
  Passed EndHud.Vision.Tests.PhysicalUltimateTests.Ready_next_to_coloured_circles_charging [35 ms]
  Passed EndHud.Vision.Tests.PhysicalUltimateTests.A_white_out_is_not_a_full_charge [21 ms]
  Passed EndHud.Vision.Tests.PhysicalUltimateTests.Three_ready_and_one_about_a_third_charged [23 ms]
Total tests: 8
     Passed: 7
     Failed: 1
```

The light effect left 0.12 white where the icon is; a ready grey circle's icon is 0.45-0.59.

## Perturbation (after the fix)

The reader set back to the one before the fix, the tests otherwise as they are (Debug):

```
  Failed EndHud.Vision.Tests.PhysicalUltimateTests.Nearly_full_charge [57 ms]
  Failed EndHud.Vision.Tests.PhysicalUltimateTests.Ready_right_after_filling [24 ms]
  Failed EndHud.Vision.Tests.PhysicalUltimateTests.Charging_over_a_light_floor [21 ms]
  Failed EndHud.Vision.Tests.PhysicalUltimateTests.Empty_again_after_the_cast [18 ms]
  Failed EndHud.Vision.Tests.PhysicalUltimateTests.Ready_next_to_coloured_circles_charging [24 ms]
  Failed EndHud.Vision.Tests.PhysicalUltimateTests.Three_ready_and_one_about_a_third_charged [21 ms]
Failed!  - Failed:     6, Passed:     2, Skipped:     0, Total:     8, Duration: 153 ms - EndHud.Vision.Tests.dll (net8.0)
```

(The two that pass are the guards: nothing grey is read at all.) Only the white-out guard taken out
(a cream arc no longer has to be lighter than the circle's centre):

```
[xUnit.net 00:00:00.78]       slot 1 read as 1.00 charged
  Failed EndHud.Vision.Tests.PhysicalUltimateTests.A_white_out_is_not_a_full_charge [22 ms]
   slot 1 read as 1.00 charged
```
