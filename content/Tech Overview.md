---
publish: true
created: 2026-02-12T17:49:43.985-08:00
modified: 2026-04-02T18:16:04.092-07:00
cssclasses: ""
---

The core of the show control system and technical backend will be fully assembled and initialized prior to the install period. The show control computer, router, networking hardware, COGS boxes, audio hardware, and power supplies will all be mounted to the same server rack for external setup before being moved behind the train car.

Technicians: please see the [Tech Routing](https://docs.google.com/spreadsheets/d/1hNpea9c83iEV9CKdvRUwMU7tv4EyQF3eoKwme37vBFU/edit?usp=sharing) documentation for information on where to make connections. Make sure to keep this up to date if any changes are made during installation.
# Technical Layout
![[Media/Technical Layout.png]]

# Notes on COGS Compatibility
All custom puzzle devices must be constructed in such a way that they can be easily connected to the COGS Masters that will be operating the majority of the electronics in the attraction. A detailed wiring/connection guide with clear labels for exactly which inputs and outputs are connected where is an expected deliverable for all contracted creative technology props.

Any device containing a low-current logic input or output must have a female RJ45 connector (wired according to the B-standard) that is accessible to the install/programming teams but inaccessible to players. These will either be connected directly to a COGS Digital Master (+5VDC logic inputs and outputs) or a COGS Sensor Master (0-5VDC analog input).

![[Media/Digital Master.png]]
![[Media/Sensor-02.png]]

All servo motors will be connected to a Servo Master, and devices requiring servo power and control should terminate in either a female RJ45 connector or a female three-wire JST connector.

![[Media/Servo-02.webp]]

All maglocks, cabinet locks, or other devices requiring a +12VDC or +24VDC power supply that can be switched on and off will be connected to a DC master.

![[Media/DC Master.png]]

# Sound
This room contains 12 speakers, and the audio backend is designed to allow for quick audio file updates on the show control Mac Mini, detailed audio mixing and routing to specific speakers in TouchDesigner, and master volume control.

Rather than using the built-in Audio Play behaviors in COGS, an OSC connection has been set up between COGS and TouchDesigner on the Mac Mini.

To play a sound, COGS sends an OSC message to TouchDesigner containing the audio filename to play as an argument. TouchDesigner then triggers the appropriate file's Audio Play In CHOP to start playing audio. The audio is then mixed and routed to specific output channels on the 2nd gen Focusrite 180i20 audio interface, routed through the appropriate amplifier channel, and played on the speaker in the room. Control of the master audio volume in the room works via the same system.

Please note that for this system to work, the Audio File In CHOPs in TouchDesigner need to be given the name of the audio file to play. It is more important that this filename match the one transmitted by COGS than that the actual audio file referenced by the OP matches the one in COGS.

For the full breakdown of available OSC messages, please refer to the [Tech Routing](https://docs.google.com/spreadsheets/d/1hNpea9c83iEV9CKdvRUwMU7tv4EyQF3eoKwme37vBFU/edit?usp=sharing) document.

# DMX

[UKING ZQ02001 Moving Head Lights](https://www.uking-online.com/products/b242-led-30w-moving-head-light-spot-color-gobos-light?variant=43855331295343) are the moving fixtures for the "lights passing the train" effect (fixture positioned in the [[Rooms/Courtyard]]) and the vaudeville spotlight effect inside the [[Rooms/Big Top (Circus Tent)]]. The manual for these fixtures, including information on all DMX channel functions, can be found [here](https://www.uking-online.com/cdn/shop/files/ZQ02001.pdf?v=536862946589303442).
# Resources
- [LED mapping via Art-Net](https://www.youtube.com/watch?v=ShYYcr30vJw&t=1s)
- [Installing COGS on Ubuntu](https://learn.cogs.show/installing-cogs-software)
- [Art-Net Receiver Node](https://github.com/mdethmers/ESP32-Artnet-Node-receiver)