---
publish: true
created: 2026-02-12T17:49:43.924-08:00
modified: 2026-03-31T14:17:22.931-07:00
cssclasses: ""
---

The interactable controller for [[Puzzles/Puzzle 8 - Inverted Pyramid]] and [[Puzzles/Puzzle 9 - Countless Eyes]].
# Deliverables
- One fully functional, robustly constructed prop ready to be connected to COGS and power with no additional setup.
# Design Specifications
- This should have the appearance of an ancient stone artifact. Think *Indiana Jones* or some sort of hidden Mayan temple.
- The wheels each have path markings on them. These should not be painted - they should be physically carved into the wheel shapes with a rotary tool or CNC router and filled with colored resin so the markings can never wear out.
# Technical Specifications
- Unlike the rotary encoders used for the [[Creative Technology/Gas Valves]], the wheels actually MUST be connected to potentiometers because the specific position of each wheel is what matters, not the relative amount it's been turned at any given time. Because the second phase of the puzzle involves using the wheels as dials to rotate the [[Props/Eyeball Growths]] in [[Puzzles/Puzzle 9 - Countless Eyes]], players will automatically reset the positions of the wheels while solving the second stage of the puzzle.
- The output signals from each potentiometer will be connected to a [COGS Sensor Master](https://run-on-cogs.myshopify.com/products/sensor-master). These typically support a single RJ45 connector input for each pair of two sensors, but if we re-route the input signals a bit it is possible to use a single connector for all six potentiometers, plus +5V and GND.
- The wheel pyramid components should connect to one labeled [female RJ45 screw terminal breakouts](https://a.co/d/06Ej4v8P) that can be easily connected to a COGS digital master with an ethernet cable. Signals should be routed as outlined below.
## RJ45 Breakout (On-Device)

| #   | Connection     |
| --- | -------------- |
| 1   | GND            |
| 2   | Wheel 1 Output |
| 3   | Wheel 2 Output |
| 4   | Wheel 3 Output |
| 5   | Wheel 4 Output |
| 6   | Wheel 5 Output |
| 7   | Wheel 6 Output |
| 8   | +5V            |
# Installation Notes
Prior to connecting to the sensor master, the single ethernet cable carrying all 6 signals will need to be split into three more cables for direct connection to the Sensor Master.

The cable connected to the puzzle should be connected to another RJ45 screw terminal breakout near the server rack and rerouted into three different RJ45 breakouts as shown below:
## RJ45 Breakout A (Near Server Rack)

| #   | Connection     |
| --- | -------------- |
| 1   | GND            |
| 2   | +5V            |
| 3   | Wheel 1 Output |
| 4   | N/A            |
| 5   | N/A            |
| 6   |                |
| 7   |                |
| 8   | Wheel 2 Output |
## RJ45 Breakout B (Near Server Rack)

| #   | Connection     |
| --- | -------------- |
| 1   | N/A            |
| 2   | N/A            |
| 3   | Wheel 3 Output |
| 4   | N/A            |
| 5   | N/A            |
| 6   | N/A            |
| 7   | N/A            |
| 8   | Wheel 4 Output |
## RJ45 Breakout C (Near Server Rack)

| #   | Connection     |
| --- | -------------- |
| 1   | N/A            |
| 2   | N/A            |
| 3   | Wheel 5 Output |
| 4   | N/A            |
| 5   | N/A            |
| 6   | N/A            |
| 7   | N/A            |
| 8   | Wheel 6 Output |
# Reference Images
