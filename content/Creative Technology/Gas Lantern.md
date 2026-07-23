---
publish: true
created: 2026-02-12T17:49:43.906-08:00
modified: 2026-07-22T18:37:36.545-07:00
cssclasses: ""
---

A mobile, interactable electronic prop taking the form of an [old-fashioned railroad-style gas powered lantern](https://www.pinterest.com/matthewpmm/hyde-circus-refresh/lanterns/). The lantern is initially trapped under the [[Creative Technology/Lantern Cage Mechanism]] in the [[Rooms/Courtyard]] and not illuminated, but it flares to life once [[Puzzles/CANCELLED - Lighting the Lantern]] is completed and it is freed. Once the [[Props/Vial of Earthly Spice]] is inserted into the lantern in [[Puzzles/Puzzle 11 - Creating Magic Flame]], it changes to a blacklight, allowing players to reveal hidden writing all around the environment.

The most pressing aspect of this prop is the programming and electronics. We may seek a separate contract to fabricate the actual exterior housing for the lantern, and it would be possible for us to fabricate additional copies of it in-house, but the initial R&D, wireless communication setup, programming and hardware experimentation would be extremely useful to outsource.
# Deliverables
- Presentation and demonstration of a fully functional prototype of the device hardware that fulfills all outlined technical specifications.
- All code written to program the device, as well as a list of any particular third-party libraries used. This includes any additional scripts or server programs designed to run on the show control computer and act as a broker between the device hardware and COGS.
- A fully sourced list of all hardware and parts used to construct the device.
- Full documentation for replicating the hardware and changing settings in code.
- Any relevant maintenance documentation for the item.
# Design Specifications
- A moderately strong magnet (or magnets) must be securely mounted to the interior bottom of the device so that the lantern can be detected by the reed switch inside the [[Lighting/Limelight]]'s lantern chamber when it is placed inside.
- All hardware inside the device needs to be securely attached to the housing and completely unable to move, even if the device is dropped, struck, or shaken.
- All wiring connections must be permanent.
# Technical Specifications
- Power
	- The device must have a rechargeable battery that does not need to be removed by game operators in order to be charged.
	- If a charging port is used, it must be a USB-C charging port rated for a typical 5VDC USB-C battery charger. Any such port may not be accessible to guests during gameplay, and must be easily accessible to game operators.
	- The device must be designed with a fast and simple method of turning the device on and off that is intuitive and provides clear feedback to game operators, but is inaccessible to players and reasonably close to impossible to be stumbled upon by players accidentally.
	- The battery life of a 
- Light
	- When in blacklight mode, this light should emit a 365nm blacklight beam to produce the best lighting results. I recommend basing it on the hardware of the [uvBeast V3 365nm flashlight](https://a.co/d/0cyexkbW).
- Sensors
	- The device must contain one [recessed-style reed switch](https://a.co/d/08yukjSM) to detect the magnet inside the [[Props/Vial of Earthly Spice]] that must be inserted into the lantern in [[Puzzles/Puzzle 11 - Creating Magic Flame]].
- Wireless Communication
	- This device must support two-way communication with COGS via one of the following methods:
		- ZigBee Radio
		- Any of the following protocols via Wi-Fi:
			- OSC
			- TCP
			- UDP
			- HTTP (see [COGS Plugin Directory](https://docs.cogs.show/plugins/))
	- If COGS cannot integrate directly with whatever protocol is used, the Contractor is responsible for providing any additional software needed to bridge the gap in communication.
	- Any networking set up must be designed to work interchangeably with any powered-on lantern devices so they can be easily switched out by a game operator in the event of battery loss, technical issues, or damage to the device.

> [!NOTE]
> For all of the specified messages below, it is not necessary that the messages be composed of the exact strings specified. However, the actual message strings or other data structures used to trigger or signal certain behaviors and triggers must be clearly explained in the deliverable documentation.

- Functionality
	- The device must respond to the following trigger messages (and optional additional message arguments, in italics) sent by COGS via network message with the specified behaviors:
		- "ping"
			- Device sends an affirmative "online" indicator message to COGS
		- "battery"
			- Device sends a message containing the current remaining battery life to COGS in a data format easily scaled between 0 and 100%.
		- "reboot"
			- The device fully reboots from either a hardware or software perspective and restarts its normal operating loop. This must include turning off all lights.
		- "light  *brightness*  *milliseconds-to-fade*"
			- Sets the main visible-spectrum white light to a specified brightness value (linearly fading up or down in brightness over the duration of milliseconds specified in its second argument). If it was not already active, this will begin a built-in, semi-random flickering animation simulating the flickering of a gas flame. This lighting animation must continue until the device reboots or receives another method changing the lighting state.
		- "blacklight  *brightness*  *milliseconds-to-fade*"
			- Sets the secondary 365nm black to a specified brightness value (linearly fading up or down in brightness over the duration of milliseconds specified in its second argument). If it was not already active, this will begin a built-in, semi-random flickering animation simulating the flickering of a gas flame. This lighting animation must continue until the device reboots or receives another method changing the lighting state.
		- "off  *milliseconds-to-fade*"
			- Fades out any lighting animation currently playing (linearly fading down in brightness over the duration of milliseconds specified in its second argument), ending any active animation loop once the fade ends.
	- The device must send the following feedback messages to COGS via network message when each of the following triggers occur:
		- "online"
			- when first connecting to the network after a reboot or powering on
			- when prompted to affirmatively signal connection status via COGS
		- "battery-life"
			- when first connecting to the network after a reboot or powering on
			- when the device's battery life crosses above or below 5%, 25%, 50%, 75%, or 95%
			- when prompted to transmit data about its current battery life by an incoming message from COGS
		- "spice-detected"
			- when the built-in reed switch detecting the insertion of the [[Props/Vial of Earthly Spice]] is triggered
# Reference Images

Please refer to the ["Lanterns" sub-board of the main Pinterest board](https://www.pinterest.com/matthewpmm/hyde-circus-refresh/lanterns/) for more reference material.

![[Media/0d81ecfec7898980703441a1eed6fc2d.jpg]]
#creative-tech #lighting #props 