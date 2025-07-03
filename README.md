# kamalot

## MIDI

### Launching Clips in Ableton Live

# Ableton Live 8×8 Grid MIDI Mapping

This document outlines the **default MIDI note mapping** for an 8×8
grid controller (such as the Novation Launchpad) when used with
**Ableton Live**. These mappings correspond to **clip launch slots**
in Session View and are automatically handled by Ableton’s built-in
Control Surface scripts.

## Grid Layout

The 8×8 grid corresponds to **MIDI Note On messages** on **MIDI
Channel 1**. The layout below shows the note numbers sent by each pad
on the controller, organized as a grid with **columns left to right**
and **rows from bottom to top**, matching the Session View in Live.

Top of Session View

+------+------+------+------+------+------+------+------+
| 91 | 92 | 93 | 94 | 95 | 96 | 97 | 98 | ← Row 8
+------+------+------+------+------+------+------+------+
| 83 | 84 | 85 | 86 | 87 | 88 | 89 | 90 | ← Row 7
+------+------+------+------+------+------+------+------+
| 75 | 76 | 77 | 78 | 79 | 80 | 81 | 82 | ← Row 6
+------+------+------+------+------+------+------+------+
| 67 | 68 | 69 | 70 | 71 | 72 | 73 | 74 | ← Row 5
+------+------+------+------+------+------+------+------+
| 59 | 60 | 61 | 62 | 63 | 64 | 65 | 66 | ← Row 4
+------+------+------+------+------+------+------+------+
| 51 | 52 | 53 | 54 | 55 | 56 | 57 | 58 | ← Row 3
+------+------+------+------+------+------+------+------+
| 43 | 44 | 45 | 46 | 47 | 48 | 49 | 50 | ← Row 2
+------+------+------+------+------+------+------+------+
| 35 | 36 | 37 | 38 | 39 | 40 | 41 | 42 | ← Row 1
+------+------+------+------+------+------+------+------+

Left → Right (Track 1 → Track 8)


- Each pad sends a `Note On` message with a unique **MIDI note number**.
- Pressing a pad launches the corresponding **clip slot** in Ableton Live.
- These mappings are active when the controller is set as a **Control Surface** in Live's preferences.

To launch the clip in **Track 3, Row 6**, press the pad that sends MIDI note **77**.


#### References

- Ableton Live → Preferences → MIDI → Control Surface
- Novation Launchpad MIDI Implementation Chart
- [MIDI Note Number Chart](https://www.inspiredacoustics.com/en/MIDI_note_numbers_and_center_frequencies)



