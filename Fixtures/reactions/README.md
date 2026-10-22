# Reaction levels

Frames chosen for the level badge on a reaction's icon in the boss's status row (`ReactionLevel`),
from the owner's recordings (3838x2158). Everything below y 320 is blacked out (that includes the
UID): only the boss's bars, the ring and the status row are kept. Found by stepping 1 s sheets of
the status row through each whole recording (never its last 5 s).

The badge is a dark square over the icon's bottom-right corner, overlapping the frame, with the
level as a Roman numeral in the reaction's colour (yellow-green for Corrosion, yellow for
Electrification), serifs at top and bottom.

`labels.json` lists, per file, a position in the row (0 = leftmost), the wiki status there (`null`
when the wiki has no such icon) and the level (`null`: no Roman numeral at that position).

| File | Recording, second | Shows |
|---|---|---|
| `corrosion-III-84s.jpg` | `battle_test2_si.mp4`, 84 | Corrosion III at 1; a digit 2 badge at 4 |
| `corrosion-III-96s.jpg` | `battle_test2_si.mp4`, 96 | Corrosion III at 0; a digit 2 badge at 3 |
| `electrification-II-36s.jpg` | `zhuang_battle3.mp4`, 36 | Electrification II at 0; a digit 2 badge at 2 |
| `electrification-II-57s.jpg` | `zhuang_battle3.mp4`, 57 | Electrification II at 1; a digit 2 badge at 3 |
| `electrification-III-91s.jpg` | `zhuang_battle3.mp4`, 91 | Electrification III at 1; a digit 2 badge at 4 |
| `electrification-IV-45s.jpg` | `fullbattletest.mp4` (Laevatain), 45 | Electrification IV at 0; Combustion (no badge) at 1; a digit 2 badge at 4 |
| `electrification-IV-71s.jpg` | `fullbattletest.mp4` (Laevatain), 71 | Electrification IV at 4; a digit 2 badge at 6 |
| `other-laevatain-27s.jpg` | `fullbattletest.mp4`, 27 | a digit 1 badge at 3 |
| `other-laevatain-33s.jpg` | `fullbattletest.mp4`, 33 | the Corrosion icon with no badge at 1; a digit 2 badge at 4 |
| `other-si-22s.jpg` | `battle_test2_si.mp4`, 22 | a digit 2 badge at 5 |
| `other-typhoeus-30s.jpg` | `typho_battle.mp4`, 30 | the Electrification icon with no badge at 1; a digit 1 badge at 4 |
| `other-zhuang-46s.jpg` | `zhuang_battle3.mp4`, 46 | the Electrification icon with no badge at 0; a digit 2 badge at 1 |

Seen in the four recordings: Corrosion III (Si, 74-110 s), Electrification II, III and IV (Zhuang
35-59, 91 and 106-143 s; Laevatain 40-111 s). No level I badge was seen. The Corrosion and
Electrification icons also show with no badge at all (Laevatain 32-35 and 107-111 s, Zhuang, and
through most of the Typhoeus fight); what level that is hasn't been confirmed, so it reads as unknown.
