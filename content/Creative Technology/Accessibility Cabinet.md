---
publish: true
created: 2026-02-24T16:37:31.809-08:00
modified: 2026-04-17T18:06:58.054-07:00
cssclasses: ""
---

This is a cabinet containing several adjustable settings controlled by buttons and dials for players to access to ensure the experience is as accessible as possible. It is modeled after the one in Big Brain Labs.
# Deliverables
- One fully constructed and labeled accessibility cabinet ready to be connected to the attraction's show control system
- Fully sourced list of replacement parts
# Design Specifications
- All text should be printed in black in a clearly readable sans serif font (i.e. Helvetica, Helvetica Neue, or Arial) on a white background
- Must contain a USB-C charging cable for the accessibility tablet.
- The inside of the door should feature descriptions of each setting and recommendations for who should and shouldn't use them.
- Must contain a fixed-in-place stand on the bottom interior surface of the cabinet for the accessibility tablet.
# Technical Specifications
- Flashing Light Effects: Momentary push-button with labeled on/off indicator LEDs (with resistors)
- Extra Light button: Momentary push-button with labeled on/off indicator LEDs (with resistors)
- Less-Scary Mode: Momentary push-button with labeled on/off indicator LEDs (with resistors)
- Background Music Volume dial: [Rotary encoder](https://a.co/d/04HXf6UK) with labeled Low/Normal/High indicator LEDs (with resistors)
- Dialogue Volume dial: [Rotary encoder](https://a.co/d/04HXf6UK) with labeled Low/Normal/High indicator LEDs (with resistors)
- Accessibility tablet: A cheap, 10" Android tablet with a USB-C charging port and sturdy black case on which we can install the [COGS Media Master app](https://play.google.com/store/apps/details?id=dog.clockwork.mobile.av)
- Must contain two internal female DC barrel jack connectors that the install team can connect the +5V and +12V supplies to power the cabinet components from.
- The USB-C charging cable must be connected to the +5V supply.
- The cabinet components should connect to 2 labeled [female RJ45 screw terminal breakouts](https://a.co/d/06Ej4v8P) that can be easily connected to a COGS digital master with an ethernet cable. Signals should be routed as outlined below.
- Must contain a [GIDERWEL 12 Channel DMX decoder](https://a.co/d/0dQWbyIB) set to address 24 and wired to all LEDs as outlined in the channel list below. This should be connected to the +12V barrel jack.
- All LEDs must be pre-connected to an appropriate resistor and rated properly to be powered by a +12V PWM supply via the DMX decoder ([consider these](https://a.co/d/00Tya8eo)).

## RJ45 Breakout 1

| #   | Connection                    |
| --- | ----------------------------- |
| 1   | Flashing Light Effects Button |
| 2   | Flashing Light Effects Button |
| 3   | Extra Light Button            |
| 4   | Extra Light Button            |
| 5   | Scaredy-Cat Mode Button       |
| 6   | Scaredy-Cat Mode Button       |
| 7   |                               |
| 8   |                               |
## RJ45 Breakout 2

| #   | Connection                            |
| --- | ------------------------------------- |
| 1   | GND (also connect to barrel jack GND) |
| 2   | BG Music Vol Dial CLK                 |
| 3   |                                       |
| 4   | BG Music Vol Dial DT                  |
| 5   |                                       |
| 6   | Dialogue Vol Dial CLK                 |
| 7   |                                       |
| 8   | Dialogue Vol Dial DT                  |
## DMX PWM Decoder

| Decoder Channel |                                   |
| --------------- | --------------------------------- |
| 1               | Flashing Light Effects Button LED |
| 2               | Extra Light Button LED            |
| 3               | Less-Scary Mode Button LED        |
| 4               | BG Music Volume Low LED           |
| 5               | BG Music Volume Normal LED        |
| 6               | BG Music Volume High LED          |
| 7               | Dialogue Volume Low LED           |
| 8               | Dialogue Volume Normal LED        |
| 9               | Dialogue Volume High LED          |
| 10              |                                   |
| 11              |                                   |
| 12              |                                   |

# Reference Images
![[Media/2.jpg]]
![[Media/1 1.jpg]]
#accessibility #creative-tech 