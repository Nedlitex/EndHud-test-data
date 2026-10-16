# EndHud test data

Screenshots and gameplay recordings that [EndHud](https://github.com/Nedlitex/EndHud)'s vision
tests read. They are kept out of the main repository so that cloning EndHud stays small; EndHud
includes this repository as an optional Git submodule at `tests/data`.

You need it only to run the vision tests:

```
git clone --recurse-submodules https://github.com/Nedlitex/EndHud.git
# or, in an existing clone:
git submodule update --init
```

Building and running EndHud doesn't need it.

## Layout

| Folder | Size | Used by |
|---|---|---|
| `Fixtures/` | ~57 MB | Single frames: combat states, squads, counters, statuses, screen-size simulations. Each subfolder's README says where its frames come from and what they show. |
| `Recordings/` | ~162 MB, Git LFS | Gameplay recordings with everything but the game's HUD blacked out (see `Recordings/README.md`). |

The test projects copy both folders next to the test binaries, so the tests open them as
`Fixtures/...` and `Recordings/...`.

## Privacy and content

All frames are from the maintainer's own play. The player UID is blacked out in every image and
recording, and file metadata is stripped. The game's art belongs to its developer and publisher;
these files are here only to test EndHud's recognition.

## Changing the data

Commit here first, then update the submodule pointer in EndHud (`git -C tests/data pull`, then
commit `tests/data` in EndHud) in the same change as the tests that need it.
