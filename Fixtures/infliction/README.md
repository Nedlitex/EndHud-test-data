# Elemental infliction ring

Frames chosen for the infliction ring at the right end of the boss's HP bar (`InflictionRing`), 4K.
`labels.json` names the infliction each one shows, or `null`, and its stack count (`stacks`: the white
arc segments around the ring, clockwise from the top; `null` when there is no ring).

`ring-*.jpg`: the same boss fight as `battle-hud/` (player UID blacked out):

- heat at one stack, and at two (`ring-69_25s.jpg`, the second white segment on the right);
- nature at one stack;
- heat at one stack under a white circle effect (`ring-99_9s.jpg`);
- none: a white background behind the ring's place, an ultimate cutscene, and two frames of blue
  effects that fill the disc's place with colour but have no white segment above it.

`si-cryo-*.jpg`: the owner's Si fight (`battle_test2_si.mp4`, 3838x2158), cut at the second in the
name (39.5, 41.5, 50.5, 51.5, 57.5, 58.25, 65.5, 67.5 and 71.5 s), picked by stepping 0.25 s
through 38-75 s. Everything below y 320 is blacked out (that includes the UID): only the boss's
bars, the ring and the status row are kept. Cryo at:

- one stack (39.5 s, 65.5 s), two (41.5 s, 67.5 s), three (51.5 s, 71.5 s), four (57.5 s; 58.25 s
  over dark leaves);
- three with a blue effect brushing the empty left segment (`si-cryo-50_5s.jpg`).

In the recording the ring shows 1 stack 38.75-40.0 s, 2 at 40.25-42.25 s, 3 at 44.25-53.5 s, 4 at
53.75-60.0 s, then (after the ring went away) 1 at 65.0-66.5 s, 2 at 66.75-70.5 s and 3 at
70.75-74.0 s. An unlit segment has no track of its own: the scene behind shows through, so a
white scene can be as bright there as a lit arc. A lit arc has a dark outline the scene doesn't.
