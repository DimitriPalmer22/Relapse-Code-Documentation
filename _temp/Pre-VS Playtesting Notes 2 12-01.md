# Pre-VS Playtesting Notes 2: 12-01

## General Notes
- I built the game before playing.
- The loading bar on the main menu works btw. Its only laggy in the editor :/
- FPS is *playable* for most of the level. FPS feels the best in Alex's level.
	- By *playable* I mean it's in the 25-60 on my laptop.
	- I can see what I can do about this.
- IN CASE THE PLAYER FALLS OUT THE MAP, a kill collider needs to be added to the bottom of the level.
- The staircase needs to be fully covered and not exposed to the void
- The new wardrobes need colliders
- We might need to change the color of the keycard prefab. It makes it a little too difficult to see with the interactable material.
- The keycard reader:
	- needs a material
	- needs the interactable material
- Vendor idle animations need to be added
### Occlusion Culling
- If possible, the debris objects should not be set as occluders because it causes too many artifacts with the occlusion culling.
- Some of the rooms are messed up in terms of occlusion culling and idk why.

### IMPORTANT FOR LEVEL DESIGNERS
- Enemies + their patrol paths need to be added to each level.
- Each floor needs to be re-navmeshed for the _
- Phone ringing zones need to be added to each level.
- Each interactable object needs the material
- Both vendors need to be interactable and have their corresponding vendor information

## 4th Floor
- The lesions enemy that's currently in this level needs to be replaced by the new prefab. (It has melee in its name, so u can just search that up to find it)
- The fat enemies need to be replaced by the new lesions enemy
- There's a wardrobe blocking the little hallway between the gun room and the phone room. 

## 5th Floor
- A lot of those lore pickups Brian on his level has that are just squares need to be disabled. 
	- We won't have enough lore items before VS to have this many. For VS, we are planning to have 1 pickup. We can add them back later though. 
	- Also, there's a prefab called "MinorMemory", which you should be using for these pickups. All you would need to do for these is create / edit a scriptable object & drag it in.
- The door for the room in Brian's level where the keycard USED TO BE needs a collider. The player can walk through it and fall out of the map.
- We need an elevator buttons model.
	- Then, we need to replace the block that's next to the elevators

## 3rd Floor
- We need elevator buttons
- In the area that has the elevators, there's a floating bucket that looks out of place
- The phone may need to be moved back to the table idk.
	- It probably won't matter when we add the interactable material + the phone sounds.
- The elevators are marked as static, so they wont visibly open when we use the keycard.
	- We *can* still go through it, though, so it isn't game-breaking
- The elevator hole needs to be bigger 
- We need a light inside the elevator shaft
- The elevator access keycard on Aiden's level needs to be replaced with the actual keycard model
- IM GETTING LIKE 5 FPS IN THE ELEVATOR AREA FOR AIDEN'S LEVEL

## Floor 2
- Noticeable FPS jump in this floor for some reason.
- I (Dimitri) need to make a script that gives you your sprinting and jumping back.
- We'll put this script on the big ass syringe on the table
	- Speaking of this syringe, it might need to be scaled down.
	- It also needs the interactable material on it
- The doctor:
	- needs to be scaled down a little. Bro has LeBron genetics.
	- needs the vendor script
	- needs the interactable material
- Phone is floating above the table
- The door at the end of the level is misaligned with the staircase.

## After Floor 2
- Andre's level section needs to be added to the end of Alex's level
- Mikel's lobby needs to be added after that.
- If for some reason we cannot add Andre's portion of the level, we can have the end of Alex's level lead into Mikel's level
