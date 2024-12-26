## Things to Standardize

For gameplay to remain consistent across the whole level, a couple things need to be solidified.

### Architecture
- Floor height across all buildings.
	- The lesion enemies are approximately 4 Unity Units tall, so each floor of each building needs to be *AT LEAST* this tall.
- Cover

### Movement System Sections
- Jump Lengths.
	- If the player is supposed to jump across a specific section of the level, having that size be consistent is a good way for the player to realize they are supposed to jump over something.
- The heights of objects the player is supposed to slide under.
	- There's a *teeny* quirk with the player controller that allows the player to just squeeze under gaps (without sliding) if the gap is tall enough (I think about 1.5 Unity Units). A gap size of 1.25 units should be fine.
- Wall-runnable / Wall-slidable surfaces
	- The appearance of wall-runnable surfaces needs to be consistent in terms of size and shape.
	- The layout of the walls the player is supposed to jump from. What I mean is, if a player reaches a wall-running segment where they need to jump from wall to wall, then the distances of the walls between each other and the lengths of each wall should be about the same between all instances of these segments.
	- Also, the player *can* use wall-jumping to scale walls vertically even more so than they already do. There are values on the player wall-running script we can play with to make them wall-jump higher / further.
