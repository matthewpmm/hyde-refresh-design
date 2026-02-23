---
publish: true
created: 2026-02-12T17:49:43.985-08:00
modified: 2026-02-17T19:04:29.226-08:00
cssclasses: ""
---

The core of the show control system and technical backend will be fully assembled and initialized prior to the install period. The show control computer, router, networking hardware, COGS boxes, audio hardware, and power supplies will all be mounted to the same server rack for external setup before being moved behind the train car.
# Technical Layout
![[Technical Layout.png]]

# Notes on COGS Compatibility
All custom puzzle devices must be constructed in such a way that they can be easily connected to the COGS Masters that will be operating the majority of the electronics in the attraction. A detailed wiring/connection guide with clear labels for exactly which inputs and outputs are connected where is an expected deliverable for all contracted creative technology props.

Any device containing a low-current logic input or output must have a female RJ45 connector (wired according to the B-standard) that is accessible to the install/programming teams but inaccessible to players. These will either be connected directly to a COGS Digital Master (+5VDC logic inputs and outputs), a COGS Sensor Master (0-5VDC analog input), or a

![[Pasted image 20260217185001.png]]
![[Creative Technology/Sensor-02.png]]

All servo motors will be connected to a Servo Master, and devices requiring servo power and control should terminate in either a female RJ45 connector or a female three-wire JST connector.

![[Creative Technology/Servo-02.webp]]

All maglocks, cabinet locks, or other devices requiring a +12VDC or +24VDC power supply that can be switched on and off will be connected to a DC master.

![[Creative Technology/DC-02.png]]
# Resources
- [LED mapping via Art-Net](https://www.youtube.com/watch?v=ShYYcr30vJw&t=1s)
- [Installing COGS on Ubuntu](https://learn.cogs.show/installing-cogs-software)
- [Art-Net Receiver Node](https://github.com/mdethmers/ESP32-Artnet-Node-receiver)