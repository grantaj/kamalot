# kamalot

## MIDI

### MIDI Out CHOP


#### Set Up Your MIDI Device

1. Open **Dialogs > MIDI Device Mapper**
2. 
   - Create New Mapping
   - Choose your MIDI device in output

#### Create a MIDI Out CHOP

1. Add a `MIDI Out CHOP` to your network
2. In the **MIDI Out CHOP parameters**:
   - Set **Output Device** to your mapped MIDI device

#### Connect CHOP Channels
The MIDI messages are controlled by the input channel, and the name of the input channel specifies the message.

For example

`ch3n60` - this channel is interpreted as channel3 note 60. A Note On event is sent when the value goes from 0 or less to greater than zero
`ch5n` - This channel will contain note numbers. The value quantized to an integer, and when the integer value changes, the note of the old value goes off and the note of the new value goes on. If the channel steps from 53 to 78, it sends a Note Off event for note 53, and a Note On event for note 78.
`ch14c7` - the value of the channel is sent to controller 7 (volume) of channel 14. By default, the values 0 to 1 are mapped to MIDI value 0 to 127.

| Purpose              | CHOP Channel Name | Meaning                                |
|----------------------|------------------|----------------------------------------|
| Note On (note 60) on channel 1  | `ch1n60`        | Note 60 on MIDI channel 1              |
| Control Change (CC1) on channel 10 | `ch10cc1`      | CC #1 on MIDI channel 10               |
| Pitch Bend on channel 2        | `ch2pb`         | Pitch Bend message on MIDI channel 2   |
| Aftertouch on channel 4        | `ch4at`         | Channel aftertouch on MIDI channel 4   |
| Polyphonic Aftertouch for note 64 on channel 3 | `ch3pa64` | Poly AT for note 64, channel 3       |
| Program Change on channel 5    | `ch5pc`         | Program Change on channel 5            |

For multiple message types, use separate `MIDI Out CHOP`s.

#### Test with MIDI Monitor or DAW

[MIDIView](https://hautetechnique.com/midi/midiview) to confirm output.



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

|     | Col 1 | Col 2 | Col 3 | Col 4 | Col 5 | Col 6 | Col 7 | Col 8 |
|-----|-------|-------|-------|-------|-------|-------|-------|-------|
| Row 8 | 91 | 92 | 93 | 94 | 95 | 96 | 97 | 98 |
| Row 7 | 83 | 84 | 85 | 86 | 87 | 88 | 89 | 90 |
| Row 6 | 75 | 76 | 77 | 78 | 79 | 80 | 81 | 82 |
| Row 5 | 67 | 68 | 69 | 70 | 71 | 72 | 73 | 74 |
| Row 4 | 59 | 60 | 61 | 62 | 63 | 64 | 65 | 66 |
| Row 3 | 51 | 52 | 53 | 54 | 55 | 56 | 57 | 58 |
| Row 2 | 43 | 44 | 45 | 46 | 47 | 48 | 49 | 50 |
| Row 1 | 35 | 36 | 37 | 38 | 39 | 40 | 41 | 42 |

Left → Right (Track 1 → Track 8)


- Each pad sends a `Note On` message with a unique **MIDI note number**.
- Pressing a pad launches the corresponding **clip slot** in Ableton Live.
- These mappings are active when the controller is set as a **Control Surface** in Live's preferences.

To launch the clip in **Track 3, Row 6**, press the pad that sends MIDI note **77**.


#### References

- Ableton Live → Preferences → MIDI → Control Surface
- Novation Launchpad MIDI Implementation Chart
- [MIDI Note Number Chart](https://www.inspiredacoustics.com/en/MIDI_note_numbers_and_center_frequencies)



