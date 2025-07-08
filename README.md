# kamalot

# MIDI

## MIDI Out CHOP


### Set Up Your MIDI Device

1. Open **Dialogs > MIDI Device Mapper**
2. 
   - Create New Mapping
   - Choose your MIDI device in output

### Create a MIDI Out CHOP

1. Add a `MIDI Out CHOP` to your network
2. In the **MIDI Out CHOP parameters**:
   - Set **Output Device** to your mapped MIDI device

### Connect CHOP Channels
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

### Test with MIDI Monitor or DAW

[MIDIView](https://hautetechnique.com/midi/midiview) to confirm output.



## TDAbleton

### TouchDesigner Setup
= Palette/TDAbleton/Live11+ (or 9 & 10 depending on Ableton version)
- `tdAbleton Package` component
   - Select Ableton Live install from dropdown
   - Click Install (without Ableton Live running)