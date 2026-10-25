# Stagger bar (失衡条)

Frames for the boss's stagger bar (`StaggerBar`): the thin bar right under the boss's HP bar, top centre.
Cut from two of the owner's recordings of the same boss (蚀影应龙队长), 3838x2158, at the second in the name:
`fb-*` from `fullbattletest.mp4`, `f2-*` from `test_battle_full2.mp4` (never from a recording's last 5 s).
Everything below y 320 is blacked out (that includes the UID): only the boss's name, bars and status row are kept.

`labels.json` gives, by eye and checked against the bar's pixels:

- `state`: `building` (the bar filling pink, whiter towards its right end), `staggered` (full: the yellow countdown
  bar draining), or `null` (no boss bar: before the fight, an ultimate's cutscene);
- `progress`: how far the pink fill reaches, as a share of the bar (the lighter part ahead of it, stagger just
  added, counts: it becomes pink a moment later);
- `countdown`: the yellow bar's length, as a share of the bar;
- `nodes`: the node boxes (失衡节点), as shares of the bar: this boss has one, at the middle; `reached`: how many the
  fill has passed (all of them while staggered);
- `swollen`: the node box is drawn about 1.5 times its size, which the game does for about a second when the fill
  reaches it (`fb-44_2s.jpg`, `f2-67_3s.jpg`): the small stagger's only cue on the bar.

The building frames: 0 (22.5 s, just after the bar appears; 88.5 s, just after a countdown ended), 0.10, 0.45 (a
lighter part ahead of the fill), 0.54 and 0.52 (the node just reached), 0.60-0.63, 0.81 (the whole fill flashing
lighter), 0.90, 0.98 (the most seen before the countdown). The countdowns: 0.97 and 0.99 (fresh), 0.89, 0.56 (twice),
0.19 and 0.09.
