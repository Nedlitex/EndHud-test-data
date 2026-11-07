# Argent Flow

Single frames from a recording of the owner's own fight at 4K (3838 × 2158, 30 fps), Argent Flow
controlled in squad slot 1, keyboard and mouse. The file name is the second the frame was taken at
(none from the recording's last 5 s). Everything is blacked out except the bottom centre
(x 1380–2460, y 1880–2158) and the bottom right (x 2860–3838, y 1680–2158: the ultimate circles
and battle-skill buttons), as in [`si`](../si/README.md). That also blacks out the UID.
`labels.json` gives, by eye, what the readers must say.

## `skill-*.jpg`: his battle-skill button (slot 1)

After his combo skill his battle skill turns into Bolt Rush for 20 s (the wiki's "Battle Skill
Change Duration", 20 s at every level). The button's icon turns from his own (a sweeping blade) to
a horse on gold, and a light-grey ring inside the button drains clockwise from 12 o'clock, as on
Si's. The horse is dim while he can't afford it and lit, with a white ring round the disc, when he
can. Casting Bolt Rush, or the ring running out, brings his own icon back. `icon` is `Original`
(his own) or `Changed` (the horse).

On horse frames `changedAt` is when the horse first showed in that window, by eye at 10 frames a
second: 20.5, 82.9, 114.5 and 136.9 s. `secondsLeft` = 20 − (time − `changedAt`). The ring the
reader measures runs about a second behind that (it reads full for the first second); the tests
allow 2 s.

- `18_5s`, `22s`, `80s`, `82s`, `95_5s`, `110_25s`, `123s`, `134s`, `141s`: his own icon.
- `21s`, `21_25s`: the horse, lit (cast at 21.4 s).
- `83s` to `92_75s`: the horse from 82.9 s (cast at 93.2 s). `83s`: a white flash over a pink
  scene; the icon may be read as unknown. `89_75s`: an effect over the ring.
- `115s` to `121s`: the horse from 114.5 s (cast at about 121.2 s).
- `137_5s` to `139_5s`: the horse from 136.9 s (cast at about 139.7 s).

`SkillRing`'s masks for his two icons were built from `18_5s` to `95_5s` only; the frames from
`110_25s` on check them.
