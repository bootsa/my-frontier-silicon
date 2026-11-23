# Changes in this fork

- Mode keys (Bluetooth, Spotify, Internet radio, DAB, FM) are looked up from the radio's own
  `validModes` list by id/label instead of hard-coded numbers. Fixes the Bluetooth switch jumping to
  FM on radios (e.g. Roberts Stream 94i) where Bluetooth is not mode 5.
- Preset dropdown prefixes use the radio's real mode labels and only cover modes the radio has.
- Modes whose preset list is identical to an earlier mode's are skipped (no duplicate
  "[radio]" / "[FM]" sets).
