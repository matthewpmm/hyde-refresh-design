---
publish: true
created: 2026-02-12T17:49:43.958-08:00
modified: 2026-09-02T16:01:58.063-07:00
cssclasses: ""
---

# Relevant Items
- [[Props/Journal Entries]]
- [[Creative Technology/Gas Lantern]]
- [[Props/Eye of the Ancient One]]
# Puzzle Specifications

Directly in front of the Engine Room furnace firebox is a 3' outer diameter cipher circle marked on the floor. The markings of the circle are UV-reactive, and are more clearly visible when highlighted by shining the [[Creative Technology/Gas Lantern]] on them. The circle contains fifteen glyphs distributed unevenly at precise positions, laid out like so:

![[Media/Cipher Circle Layout.jpg]]

> [!NOTE]
> These glyphs are rotated so that the bottom of each glyph points towards the center of the circle, and the top of each points radially outward.

Once guests collect all five of the [[Props/Journal Entries]]/notes found throughout the experience, they can be placed face down and assembled into a single complete pentagon with crisp, straight edges. Each of the corners of the pentagon is clearly highlighted. There is exactly one orientation of the notes where all of these highlighted corners specifically point out five total glyphs.

When the journal entries are correctly positioned, the entire circle is laid out as follows:

![[Media/Engine Cipher Layout_Cipher Circle and Notes Solved Layout.jpg]]

On the face of the furnace, there are three large rotating valves, each of which is surrounded by stones etched with five of the fifteen glyphs found on the cipher circle. They are positioned like so:

![[Media/Engine Cipher Layout_Valve Positions.jpg]]

From left to right, each of the valves is surrounded by each of the specific glyphs in this layout:

![[Media/Valve Glyph Layout.jpg]]

Two of the glyphs surrounding the left and right valves are always glowing. Only one of the glyphs surrounding the center valve is glowing.

Rotating each valve clockwise or counterclockwise causes the glowing lights illuminating the glyphs surrounding that valve to rotate around the circle, illuminating other glyphs.

The left and rightmost valves' two illuminated glyphs will scooch clockwise or counterclockwise based on which direction the valve has been rotated, alternating between having and not having a gap between the glowing glyphs. There is never a gap of more than one glyph. (See below example.)

![[Media/Valve Rotation Example.jpg]]

Players must use the notes in the cipher circle to identify which five glyphs need to be selected, then rotate each valve to correctly light up the respective glyphs. The final solution state is follows:

![[Media/Engine Cipher Layout_Valves, Glyphs.jpg]]

When the correct glyphs are illuminated, a jet of fog bursts from the firebox and the firebox door pops open, accompanied by various sound effects. To finally solve the puzzle, the [[Props/Eye of the Ancient One]] must be inserted into the firebox and the door must be closed.

> [!NOTE]
> The set of 15 glyphs used in this puzzle are letters selected from the [Phoenician alphabet](https://en.wikipedia.org/wiki/Phoenician_alphabet). This alphabet has 22 letters total but 7 are unused for this puzzle.

![[Media/Pasted image 20260901161423.png]]
# Build Specifications
- The valves we are using are QUITE HEAVY and need to be secured properly so guests can't damage the face of the furnace by leaning on them or pulling them too hard!!!
- Tech
	- We will use an Arduino MEGA with screw terminal shield to accept inputs from the valves and program the glowing glyph lights. It will be connected to an W5500 Ethernet module to communicate with COGS via OSC.
	- The LED lights will be the individually addressable string light modules I've provided. These should run off of 5V power, but please double check before hooking them up.
	- To read the position of the valves, we will cannibalize the hardware used in the gas pipe valves and adapt them to the new valves. The gas pipe valves use AS5600 magnetic encoders, which tracks the absolute rotation of a magnetic field provided by a magnet embedded in the rotating shaft, and outputs it as an analog value. They only need an analog channel, +5V, and GND.
	- COGS Communication
		- The networked Arduino MEGA must respond to the following trigger messages (and optional additional message arguments, in italics) sent by COGS via network message with the specified behaviors:
			- "ping"
				- Device sends an affirmative "online" indicator message to COGS
			- "reboot"
				- The device fully reboots from either a hardware or software perspective and restarts its normal operating loop. This must include turning off all lights.
			- "runes-on"
				- The device turns on all glowing rune lights. 
			- "runes-off"
				- The device turns off all glowing rune lights.
		- The device must send the following feedback messages to COGS via network message when each of the following triggers occur:
			- "online"
				- when first connecting to the network after a reboot or powering on
				- when prompted to affirmatively signal connection status via COGS
			- "valve-turned *valve-number direction*"
				- Valve numbers may be either zero- or one-indexed, but this must be CLEARLY DOCUMENTED.
				- Valve number must be an integer. Direction must be a boolean value of 1 indicating that the valve has been rotated one cycle clockwise or a 0 indicating that the valve has been rotated one cycle counterclockwise.
- Cipher Circle
	- The cipher circle should be etched/routed/Dremeled into the floor directly in front of the engine. It should have an outer diameter of approximately 3'.
	- The grooves cut for the circle should be filled with epoxy resin mixed with blacklight-reactive pigment. Ideally, the runes themselves should be a different color of pigment than the outline of the circle to make them stand out even more.