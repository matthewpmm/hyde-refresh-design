---
publish: true
created: 2026-02-12T17:49:43.926-08:00
modified: 2026-09-03T12:22:25.882-07:00
cssclasses: ""
---

All in-game hints are delivered in the form of audio by [[Creative Technology/The Contortionist]]. There are two [[Creative Technology/Hint Bell\|Hint Bells]] in the world, and guests can request hints by ringing them - one is a desktop call bell next to the [[Creative Technology/Contortionist's Crystal Ball]] in the [[Rooms/Passenger Car]] and one is hanging from a wall next to the Contortionist herself. If the call bell is rung during [[Puzzles/Puzzle 2 - Steam Whistles]], the Contortionist will "speak" through the crystal ball, which will illuminate while she speaks. After the first puzzle, only the hanging bell will work, and the Contortionist herself will speak to players (audio plays through the speaker behind her).

The system auto-detects which puzzle(s) are active at the time a hint is requested and auto-plays the next programmed hint in the sequence. If players exhaust all hints for any particular puzzle, a notification light will become visible to GMs in the COGS interface to alert them that players need help. Once all hints are exhausted, the last hint will be repeated until the puzzle is solved or a Game Master intervenes with more direct instructions.

> [!NOTE]
> If players attempt to ring a hint bell during dialogue or any scripted theatrical moment, nothing will happen and no hint will be triggered.
# Puzzle Hints
- [[Puzzles/Puzzle 1 - Opening the Tarot Table]]
	1. "Travelers, seven of the Fortune Teller's tarot cards are scattered about the cabin. Have you found them all?"
	2. "Look closely at this crystal ball. You may notice symbols that can be found elsewhere on this train."
	3. "Travelers, you must place the four correct tarot cards on the stand by the window in the right order. If you find which card is related to each poster with a moon symbol painted on it, you will know the correct four cards to use."
- Tarot Table SOLVED, steam valve NOT TURNED
	1. "You've found the broken valve handle! There is a hole in the wall near the brake lever and turn it!"
- [[Puzzles/Puzzle 2 - Steam Whistles]]
	1. "You have restored the flow of steam to the whistles! Now you must find the correct order to pull them."
	2. "Remember, travelers, that the *ticket* to success on a journey is to never forget your *map*."
	3. "Travelers, look at the back side of your ticket. Is there anywhere you can position it where all the punched holes are filled by symbols?"
-  When the brake lever is unlocked:
	1. "Travelers, the brake lever has been freed! Quickly, pull it to stop the train!"
	2. "Pull the lever! Now!"
- [[Puzzles/Puzzle 3 - The Gas Pump]]
	- Before the pump is activated:
		1. (if not yet activated) "Travelers, beneath me there is a mechanical device that can pump fuel. Insert a gasoline canister into it cap-first to activate it."
	- When the pump has been activated but the Pickled Punks have not been:
		1. "Rotate the valves on the wall to change the direction in which the gas flows. The gas must flow to an exhibit to unlock it."
- [[Puzzles/Puzzle 4 - Pickled Punks]]
	1. "Travelers, there should be four jars in the tent that you can move. Can you determine which spot on the pedestal they belong in?"
	2. "The four jars contain a shrunken, black heart, a six-fingered hand, a lung pierced by a blade, and a collection of teeth. Who do you think each of these belong to?"
- [[Puzzles/Puzzle 5 - Lighting the Limelight]]
	1. ""
	2. 
	3. 
- [[Puzzles/Puzzle 6 - Wheel of Death]]
	- If the limelight has not been unlocked yet:
		1. "Travelers, you would do well to re-route the flames elsewhere first. Activate the light in the middle of the grass to get a better view of your surroundings.
		2. "Travelers, which constellations correspond to things in this area? What do they have in common?"
		3. "There are four knives, and four things outside this circus that also have a knife in them. Identify what those are and you will know what constellations on the wheel to pierce. Perhaps check the tent one more time."
- [[Puzzles/Puzzle 8 - Inverted Pyramid]]
	1. "Travelers, focus on the triangular device mounted to the wall of the hall of mirrors. What markings are on it?"
	2. "You must turn the wheels until all the paths are connected, with no dead ends."
- [[Puzzles/Puzzle 9 - Countless Eyes]]
	1. "Travelers, what happens to the eyes on the other side of the mirror when you twist the wheels on the triangle?"
	2. "When the eyes on the pillars face each other, they light up. What would happen if they all were to light up?"
	3. "Keep in mind that the eyes also light up when looking at their own reflection in the mirror..."
- [[Puzzles/Puzzle 10 - Unlocking the Ringmaster's Chest]]
	1. "The Ringmaster always kept his chest locked up tight. Maybe something in there will help you find the code to unlock it?"
	2. "Those eyes staring at you from around the circus tent... how many must there be?"
	3. "Don't forget to look inside the display case under the red cloth, travelers. Perhaps it will contribute to finding the passcode to the lock."
- [[Puzzles/Puzzle 11 - Creating Magic Flame]]
	1. "The ringmaster must have left some sort of note behind to explain his motives. Find it and read it carefully."
	2. "This puzzle box seems intriguing. Maybe you can find a creative way to open it?"
	3. "Try placing the box on the floor and spinning it quickly before removing the lid."
- [[Puzzles/Puzzle 12 - Obtaining the Eye]]
	1. "Read the messages on the walls carefully, travelers."
	2. "That piece of jewlery from inside the puzzle box seems very conspicuous. Perhaps you can use it to unlock a secret?"
	3. "Travelers, shine the lantern on the display pedestal with the eye inside. Does anything stand out in the magical light?"
- [[Puzzles/Puzzle 13 - Returning the Eye]]
	1. "Travelers, you must return the eye! But first you must open the furnace door. Shine the lantern at the floor. Those runes must be necessary to cast a spell of some sort."
	2. "My fellow circus troupe members have left notes throughout the circus - five of them in total. Have you found all five? Can you combine them in some way?"
	3. "You can assemble the notes you've found in the magic circle. Is there a position to which you can rotate the shape they form to indicate five unique runes?"
# Time Checks

After a certain amount of gameplay time has elapsed, a bell tolling sound effect will automatically play, followed by a verbal time check from the Contortionist (through whatever means she is currently communicating with guests).

> [!NOTE]
> We NEED to program this in such a way as that if a time check threshold is reached while some other dialogue or scripted theatrical moment is in progress, the check audio waits until the event has concluded to play.
## Time Check 1

The sound of a bell tower chimes once, and the Contortionist's voice is heard.

> "Travelers, you must make haste. Only 45 minutes remain before escape will become impossible."
## Time Check 2

The sound of a bell tower chimes twice, and the Contortionist's voice is heard.

> "Travelers, you must make haste. Only 30 minutes remain before your time runs out."

## Time Check 3

The sound of a bell tower chimes thrice, and the Contortionist's voice is heard.

> "Travelers, your time is running out. Only 15 minutes remain before you become trapped here forever."
## Time Check 4

The sound of a bell tower chimes five times, while the Contortionist yells over it.

> "Only five minutes remain, travelers! You must hurry!"