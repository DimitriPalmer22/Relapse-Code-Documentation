Alright I played it for a while and here's my feedback:

- Overall, this is much more of what I originally had in mind for the game. I found myself actually needing to use the powers because I was feeling overwhelmed.
### Difficulty
- Right now, I think the arena feels a little too hard. And no, I'm not just bad at the game. Here are some possible fixes
	- The guns need to be more powerful
	- The melee enemies need to be a *teeny* bit slower
	- There need to be less enemies altogether
	- The enemies need to do less damage
	- The melee enemies are still coded a little ass. Ideally, I would like them to keep moving as they attack, but we don't have the animations for that rn.
- Whichever one of these we choose (if we do choose one), we have to make sure the rest of the game still feels good after the change. We wouldn't want the apartment level to feel too easy cuz of something we do here.
- Or maybe we can look at the arena as it is now as like an end-game arena that supposed to be hard. In that case, we can use this as a reference point and have the earlier arenas be easier.

### Movement & Architecture
- I like the way the level is built. Visually, it is obvious that the player is about to enter a combat space.
- In terms of the cover objects,
	- I like the variety that we have. Some objects are tall and some are short. I like the short ones cuz they allow the player to shoot over them while making the enemies walk around. Maybe we could use more of these idk. I will say tho, the short objects could be a *teeny* bit shorter so its even easier for the player to shoot over them
	- As a whole, I think the cover objects are a little too thick. The area felt a little congested at times when I was trying to walk around.

### Things that Might Need to Be Fixed / Changed
- That first animation with the gates going up is a little too slow. The player could immediately run over the gate before it goes all the way up.
- I think we should have the enemies start inside the arena instead of outside. This way, the player can see all the enemies they're about to fight and plan accordingly.
- Also, we should probably set up patrol points for the enemies so that when they lose sight of the player, they don't just stand around. They should walk around the arena and look for the player.
- I like the fact that you incorporated the slide as a part of the level's design, but I think where you put it should be moved.
	- I'm assuming the enemies won't be able to walk past the gate that the player has to slide under. If that's the case, then the player would be able to immediately slide under the gate and the enemies wouldn't be able to follow. This would make the level too easy.
	- Instead, we could:
		- Have the slide area be a door that reacts to level so that the player has to clear out a certain number of enemies before it opens
		- Have the slide area be a door that opens after like 30 seconds
		- Move the slide entirely. We could replace it with a door and place the slide somewhere away from the arena's critical path so that the player can't just slide under the gate and avoid the enemies. Maybe we could put it in a side room or something idk.
- The wall-running is a little too sensitive. I found myself wall-running when I didn't want to a couple of times. I've been planning to fix this for a while, but I've got a couple things backlogged for now. I'll get to it eventually.
- Right now there is a small bug when the player dies and presses the respawn button. What happens is that the enemies will stack on top of each other when the scene loads again. This is because I'm in the middle of reworking the loading and saving system. I'll fix this soon.
