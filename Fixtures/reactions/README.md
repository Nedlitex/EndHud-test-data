# Reaction levels

Frames chosen for the level badge on a reaction's icon in the boss's status row (`ReactionLevel`),
from the owner's recordings (3838x2158). Everything below y 320 is blacked out (that includes the
UID): only the boss's bars, the ring and the status row are kept. Found by stepping 1 s sheets of
the status row through each whole recording (never its last 5 s).

The badge is a dark square over the icon's bottom-right corner, overlapping the frame, with the
level as a Roman numeral in the reaction's colour (yellow-green for Corrosion, yellow for
Electrification), serifs at top and bottom.

At level I the game draws no badge at all (the owner's answer, 2026-10-22): a Corrosion or
Electrification icon with no badge is level I.

`labels.json` lists, per file, a position in the row (0 = leftmost), the wiki status there (`null`
when the wiki has no such icon) and the level (`1` for a Corrosion or Electrification icon with no badge;
`null`: another badge, or a status whose level isn't read). `hard`: an effect, a dim badge or a dark
scene; the level may read as unknown, but never as anything else.

| File | Recording, second | Shows |
|---|---|---|
| `corrosion-III-84s.jpg` | `battle_test2_si.mp4`, 84 | Corrosion III at 1; a digit 2 badge at 4 |
| `corrosion-III-96s.jpg` | `battle_test2_si.mp4`, 96 | Corrosion III at 0; a digit 2 badge at 3 |
| `electrification-II-36s.jpg` | `zhuang_battle3.mp4`, 36 | Electrification II at 0; a digit 2 badge at 2 |
| `electrification-II-57s.jpg` | `zhuang_battle3.mp4`, 57 | Electrification II at 1; a digit 2 badge at 3 |
| `electrification-III-91s.jpg` | `zhuang_battle3.mp4`, 91 | Electrification III at 1; a digit 2 badge at 4 |
| `electrification-IV-45s.jpg` | `fullbattletest.mp4` (Laevatain), 45 | Electrification IV at 0; Combustion (no badge) at 1; a digit 2 badge at 4 |
| `electrification-IV-71s.jpg` | `fullbattletest.mp4` (Laevatain), 71 | Electrification IV at 4; a digit 2 badge at 6 |
| `electrification-IV-107s.jpg` | `fullbattletest.mp4` (Laevatain), 107 | Electrification IV at 0 over a black scene; Corrosion with no badge at 1 (`hard`: dark scene) |
| `electrification-IV-107_47s.jpg` | `fullbattletest.mp4` (Laevatain), 107.467 | Electrification IV at 0, dim, over a black scene: the V's arms stay apart low down (`hard`: may read as unknown, never as III); Corrosion with no badge at 1 (`hard`) |
| `other-laevatain-27s.jpg` | `fullbattletest.mp4`, 27 | a digit 1 badge at 3 |
| `other-laevatain-33s.jpg` | `fullbattletest.mp4`, 33 | the Corrosion icon with no badge at 1; a digit 2 badge at 4 |
| `other-si-22s.jpg` | `battle_test2_si.mp4`, 22 | a digit 2 badge at 5 |
| `other-typhoeus-30s.jpg` | `typho_battle.mp4`, 30 | the Electrification icon with no badge at 1; a digit 1 badge at 4 |
| `other-zhuang-46s.jpg` | `zhuang_battle3.mp4`, 46 | the Electrification icon with no badge at 0; a digit 2 badge at 1 |
| `level-I-typhoeus-24s.jpg` | `typho_battle.mp4`, 24 | Electrification with no badge (I) at 0 |
| `level-I-typhoeus-46s.jpg` | `typho_battle.mp4`, 46 | Electrification with no badge (I) at 0, the brightest background seen; a digit 2 badge at 1 |
| `level-I-typhoeus-70s.jpg` | `typho_battle.mp4`, 70 | Electrification with no badge (I) at 0 over a dark scene (`hard`: a badge there would be dark on dark, so unknown) |
| `level-I-typhoeus-98s.jpg` | `typho_battle.mp4`, 98 | Electrification with no badge (I) at 0 over a dim scene |
| `level-I-typhoeus-143s.jpg` | `typho_battle.mp4`, 143 | Electrification with no badge (I) at 0 over a dim, reddish scene |

Seen in the four recordings: Corrosion III (Si, 74-110 s), Electrification II, III and IV (Zhuang
35-59, 91 and 106-143 s; Laevatain 40-111 s). No level I badge was seen. The Corrosion and
Electrification icons also show with no badge at all (Laevatain 32-35 and 107-111 s, Zhuang, and
through most of the Typhoeus fight): that is level I. It reads as I only where the badge is clearly
absent (the corner shows the icon square's own background, hardly any dark); over a dark scene, where a
badge would be dark on dark, it stays unknown.
