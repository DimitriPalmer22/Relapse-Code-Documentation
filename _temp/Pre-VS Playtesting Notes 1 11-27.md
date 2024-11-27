# Pre-VS Playtesting Notes 1 11-27

## General Notes
- The player starts with powers, but they're not supposed to. I'll fix this in the prefab.
- Get rid of ALL the on-screen UI elements that are on the gauntlet
- The player's speed needs to be lowered
- Replace the old chairs w/ the new, textured one.
- Same with the tables.
- Same with any bottles
- Same with any couches
- The placeholder enemies need to be replaced. But first, a prefab needs to be made. I can do this.

## 4th Floor
- FIX THE FLOOR COLLIDERS. The player be bouncin n shit
- Mikel's level still needs the in-between areas to be set dressed
- These areas need to be lit too (or not idk)
- In one of the rooms on the 4th floor, theres a wardrobe that makes it hard to see the hole in the wall the player needs to go through 
	- Also, we need a wardrobe model!!!
- We NEED those elevator doors for the other staircase. As of right now, the 2nd staircase allows the player to go from floor 4 to floor 3 directly, making floor 5 optional.
- Right next to the staircase that leads the player to floor 5, there is a floating trashcan
- Replace the crowbar w/ the actual model

## 5th Floor
- Brian's critical path makes it so that the dealer on floor 5 is easy to miss. The player *can* find the dealer cuz the path is lit up, but there's no guarantee that the player gets to it.
- Elevator doors need colliders
- The button for brian's elevator doesnt work w/ the outline shader. Maybe we need to use a basic cube instead for it

## 3rd Floor
- When landing on the 3rd floor, the elevator doors need to be open. (Far Left)
- Each board that covers the hole needs the outline material
- When dropping from brian's floor to Aiden's floor, the elevator for the 3rd floor also has a hole, so it's super easy for the player to drop from floor 5 to floor 1 type shit. (Maybe put the actual elevator on floor 3)

## 2nd Floor
- 2nd floor occlusion culling issues are *bad*.
	- Shit is popping in and out even when its right in front of you.
	- Unplayable FPS as well
- The backrooms area in Alex's level needs to be darkened so that the player knows not to go there
- The "MoveOnTrigger" script that moves the enemy that comes from the wall needs its inspector fields to be set. As of right now, it does not work.
- In the hallway where u see the monster pop out, we probably dont need the 2 tables next to the door that block it off. They just make it hard to get inside the room.
- In the room that has the briefcase, put something in there idk
- In the maintenance shaft, add the metallic texture
- We need to put a doctor in the room with all the drugs behind the desk or something
- Replace the cylinder models with syringes
- Replace the big ass green cylinder with an interactable syringe that gives the player the regen drug + gives them back their movement
