## Things to Standardize

For gameplay to remain consistent across the whole level, a couple things need to be solidified.

### Architecture
- Floor height across all buildings.
	- The lesion enemies are approximately 4 Unity Units tall, so each floor of each building needs to be *AT LEAST* this tall.
	- So, the floor would be 1 unit tall, the walls would be 4 units tall, and the ceiling would be 1 unit tall for a total of 6 units.
- Cover objects in the combat areas need to be consistently sized, spaced, and arranged between combat areas.

### Movement System Sections
- Jump Lengths.
	- If the player is supposed to jump across a specific section of the level, having that size be consistent is a good way for the player to realize they are supposed to jump over something.
- The heights of objects the player is supposed to slide under.
	- There's a *teeny* quirk with the player controller that allows the player to just squeeze under gaps (without sliding) if the gap is tall enough (I think about 1.5 Unity Units). A gap size of 1.25 units should be fine.
- Wall-runnable / Wall-slidable surfaces
	- The appearance of wall-runnable surfaces needs to be consistent in terms of size and shape.
	- The layout of the walls the player is supposed to jump from. What I mean is, if a player reaches a wall-running segment where they need to jump from wall to wall, then the distances of the walls between each other and the lengths of each wall should be about the same between all instances of these segments.
	- Also, the player *can* use wall-jumping to scale walls vertically even more so than they already do. There are values on the player wall-running script we can play with to make them wall-jump higher / further.
	- *ALSO*, the way we, the developers, implement wall-running needs to be consistent across all sections that require it. For objects that can be wall-run on, we should not just make the model of the object the wall-run layer and call it a day. This leads to quirks in the wall-running system. What we should be doing is putting invisible box colliders as children of these objects and making them the wall layer. This way, we get consistently smooth wall-running.

## The Anatomy of a Combat Encounter

Making combat arenas is hard and can take a lot of time. The worst part about this is that the player can probably clear a combat situation in like 30 seconds if it just has a bunch of enemies placed around. So, instead of making *MORE* combat arenas to fill out the level, we can increase the amount of time the player spends in each combat arena.

### Making Combat Arenas Take Longer
- Have mini-objectives the player needs to complete in a combat area to progress.
- This can mean:
	- finding a key to open a specific door
	- having to interact with multiple items in the area to progress
	- having very simple puzzles in the game that need to be solved to progress
- It should be noted that the objective of the level should be clearly stated to the player so they aren't aimlessly shooting at enemies.
- We can also introduce waves of enemies in the combat arenas instead of just one set of enemies that spawn in.
	- For example, the player walks into a combat arena and clears all the enemies that are initially there. Then, the player interacts with some item, and all of a sudden, a completely new set of enemies spawn in. This can be done multiple times in a single combat arena depending on what the arena wants from the player.
- We can also have enemies spawn indefinitely until the player completes a specific objective in the area. This ensures that the challenge of the game stays consistent and the player is always on their toes.
