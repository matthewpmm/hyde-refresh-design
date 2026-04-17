---
publish: true
created: 2026-02-12T17:49:43.923-08:00
modified: 2026-04-17T00:07:30.854-07:00
cssclasses: ""
---

This is one of the centerpiece set pieces of the entire experience. It is a large spinning wheel with a corpse attached to it (although this will be assembled separately).

The wheel will be divided into 13 sections, each of which is associated with and labeled by one of 13 fictional constellations:
- The Star
- The Crescent Moon
- The Big Top
- The Ringleader
- The Ape
- The Clown
- The Acrobat
- The Tall Man
- The Seal
- The Eye
- The Specimen
- The Contortionist
- The Shackles

Of the 13 constellations on the wheel, five are functionally covered by the corpse, leaving eight constellations open to have slots on them. See the layout reference image below for which sections should have knife slots.
# Deliverables
- A fully functional "wheel of death" prop that will work immediately once connected to power and COGS.
- A guide for maintaining or repairing the device.
- A fully sourced list of components used.
# Design Specifications
- Dimensions: 5' diameter wheel, elevated 1-2' above the floor, 3-6 inches thick
- This does NOT have to be a perfect circle. In fact, if it looks a little rough and hand-cut around the edges, that might even be preferable to a perfect circle, provided the edges are properly sanded and finished.
- This could EITHER have a standing base fastened to the concrete floor by bolts OR we could make do with it being fixed to one of the set walls.
- The layout of the paint job will eventually look approximately like the image below. The skeleton is positioned approximately where the corpse will eventually be attached, with its arms and legs tied to the top and bottom of the wheel.
- There should be 11 knife slots total.
- When placed in a slot, knives should not easily fall out when the wheel rotates.
![[Media/Wheel of Death Layout.jpg]]
![[Media/Wheel of Death Constellations.png]]
# Technical Specifications
- Although only four knives must be inserted to solve the puzzle, all slots must have sensors and outputs so GMs can track player behavior.
- Slots should use some sort of optical sensor to detect when a knife has been inserted, such as a break-beam sensor.
- The wheel needs to be able to freely rotate 360 degrees continuously.
- The entire device needs to rotate very slowly, no more than once every 10-20 seconds.
- The device should not be easily broken by players attempting to spin the wheel on purpose or stop the wheel while the motor is spinning.
- The motor that rotates the wheel should be able to be turned on or off by a relay, MOSFET, or other similar controller.
- The sensors and relay input should connect to 3 labeled [female RJ45 screw terminal breakouts](https://a.co/d/06Ej4v8P) that can be easily connected to a COGS digital master with an ethernet cable. Signals should be routed as outlined below.
- Any DC power inputs required to operate the device should be connectable via a barrel jack. Any AC power inputs required to operate the device should be connectable via a standard NEMA AC plug.
- All electrical hardware, gears, and connectors should be inaccessible to players but accessible to maintenance technicians and the installation crew. There should be a hole somewhere where cables can be run to connect to internal hardware during installation.
## RJ45 Breakout 1

| #   | Connection                       |
| --- | -------------------------------- |
| 1   | GND                              |
| 2   | 5V input Signal - to motor relay |
| 3   |                                  |
| 4   | Sensor 1                         |
| 5   |                                  |
| 6   | Sensor 2                         |
| 7   |                                  |
| 8   | Sensor 3                         |
## RJ45 Breakout 2

| #   | Connection |
| --- | ---------- |
| 1   |            |
| 2   | Sensor 4   |
| 3   |            |
| 4   | Sensor 5   |
| 5   |            |
| 6   | Sensor 6   |
| 7   |            |
| 8   | Sensor 7   |
## RJ45 Breakout 3

| #   | Connection |
| --- | ---------- |
| 1   |            |
| 2   | Sensor 8   |
| 3   |            |
| 4   | Sensor 9   |
| 5   |            |
| 6   | Sensor 10  |
| 7   |            |
| 8   | Sensor 11  |
# Reference Images
![[Media/8e39e5aeb03647792e67b0642decf0d2.jpg]]
![[Media/7eeb8b6b9db605cc810419c0c0484389.jpg]]
![[Media/de2e33e76e9d3f6d848de3744b657493.jpg]]