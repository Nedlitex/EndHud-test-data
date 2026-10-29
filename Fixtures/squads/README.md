# Squad screenshots

One 4K screenshot per squad, nine squads covering 32 of the 34 playable operators (some appear twice),
and for Si two frames of the owner's 4K Si recording, kept in
[`portrait-counters`](../portrait-counters/README.md) (UID already blacked out): `si-40s` with her
damage stacks drawn on her portrait and `si-70s` without. Her other slots aren't labelled (`""`), so
they give no reference. Argent Flow has no screenshot yet.
Only the squad panel is kept (bottom-left 1100×430, the rest black) and the ping/UID line under
it is blacked out. `squads.json` names the operator in each slot, by eye against the wiki avatars.

They're used two ways:

- **Tests** ([`OutOfTheBoxRecognitionTests`](../../OutOfTheBoxRecognitionTests.cs)): every squad
  is named, with nothing taught, at several screen sizes.
- **EndHud's built-in portrait references**
  ([`src/EndHud.Vision/Assets/operator-portraits.json`](../../../../src/EndHud.Vision/Assets/operator-portraits.json)):
  the character model's description of each operator's in-game portrait, at the common portrait
  sizes. Numbers only; no image is shipped. Rebuild after adding or changing a screenshot:

  ```
  dotnet run --project src/EndHud.Cli -c Release -- build-portrait-references tests/data/Fixtures/squads/squads.json src/EndHud.Vision/Assets/operator-portraits.json
  ```

A new operator needs nothing here to be recognised (EndHud falls back to the wiki avatar), but a
screenshot with them in the squad, added to `squads.json`, makes it more reliable.
