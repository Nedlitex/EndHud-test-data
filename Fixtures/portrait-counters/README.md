# Counters on the squad portraits

While an operator with a counter isn't controlled, the game draws that counter small on their
squad portrait, at its lower left: the same drawing as beside the HP bar, about 0.7 the size.

Single frames from four recordings of the owner's own fights at 4K (3838 × 2158, 30 fps), keyboard
and mouse, none from a recording's last 5 s. The file name is the operator and the second the frame
was taken at. Everything is blacked out except the squad panel (x 0–1000, y 1640–2158) and the
bottom centre (x 1380–2460, y 1880–2158: the HP bar and skill points); the UID (x 190–520,
y 2090–2140) is black too. The counters sit at y 1910–1965, well above it.

The Typhoeus recording is 2154 high: it lost its bottom 4 rows (its HP bars are at the same rows,
1986–1997, as in the 2158-high ones). Its frames have them back, black, so the HUD is where the
game draws it.

| Files | Squad (slot 1–4) | Controlled | What the portraits show |
|---|---|---|---|
| `si-*` | Si, –, –, – | 2 | Si's damage stacks: 0 is the hollow green flower, then a green cross with a white number (1–27 here). No badge drawn at all, in combat, is 0 too (owner, 2026-10-23): `28s`, `29s` (red scenery behind the corner), `70s`, `75s`. Unknown, the portrait tinted, dimmed or the fight ending: `65_5s` and `66s` (tinted red), `69s` (dimmed). |
| `laevatain-*` | –, Laevatain, Si, – | 4, then 2 from `69_5s` | Laevatain's Melting Flame: four petals, 0–3 white with I–III, 4 all pink with IV. Si's stacks in slot 3; no badge, so 0: `20s`, `38_5s`, `42s`, `45_5s`, `55_5s`. Unknown: `55s` (a white flash over the bottom of Si's), `57s` (the portraits faded, see-through). |
| `typhoeus-*` | Typhoeus, –, –, – | 2 | His Hunting Arrows (four slanted bars, one cyan per arrow) and Signs (eight dots, one white per Sign, from the bottom row up, left first). `10s` and `23_5s`: the flash when the arrows fill, over the whole icon (unreadable). |
| `zhuang-*` | Zhuang Fangyi, –, –, – | 2 | Her Sunderblades: the nine-cell diamond, one cyan per sword, the count printed beside it. `49_5s`: an effect line over it. |

`laevatain-18s`, `typhoeus-73s`, `zhuang-12s`, `zhuang-70s`: out of combat (before the fight, or
as it ends). The level text is under the portraits and no counter is drawn; at `typhoeus-73s` the
dimmed portrait looks like grey bars and dots.

`labels.json`, by eye on enlarged crops: per file the squad (`""` for an operator without a
counter), the controlled slot, whether it's in combat, and per counter on a portrait its value.
`value: null`: must read as unknown (a tinted, dimmed or faded portrait, a flash over it, the fight
ending). `noBadge: true`: Si's 0 shown by no badge at all on her clear portrait, rather than the
hollow flower. `unreadable: true`: the flash covers it; the readers may say the value or nothing,
never another number.

None in the controller layout: none of the recordings uses it.
