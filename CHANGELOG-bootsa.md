# Changes in this fork

- Mode keys (Bluetooth, Spotify, Internet radio, DAB, FM) are looked up from the radio's own
  `validModes` list by id/label instead of hard-coded numbers. Fixes the Bluetooth switch jumping to
  FM on radios (e.g. Roberts Stream 94i) where Bluetooth is not mode 5.
- Preset dropdown prefixes use the radio's real mode labels and only cover modes the radio has.
- Modes whose preset list is identical to an earlier mode's are skipped (no duplicate
  "[radio]" / "[FM]" sets).

## merged-prs branch
Includes upstream pull requests #5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 20, 21, 22
(not #19, the larger runtime_data refactor). Local changes on top: mode_key lookup for the
Bluetooth/Spotify switches, GET_MULTIPLE batched in groups of 8 for the Roberts Stream 94i.
