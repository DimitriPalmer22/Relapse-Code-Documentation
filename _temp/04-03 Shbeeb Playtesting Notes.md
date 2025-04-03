# 04-03 Shbeeb Playtesting Notes

### General Notes

- Scale audio logarithmically

- Screen shake for pistol is a lil crazy. needs to be scaled down a little
	- Disorienting at close quarters 
- Bad framerate in combat1, floor2: solution -> bake lights
- Fix the shader that's around the arenas. You can still see it even when the walls aren't up
- Death bug (might be tied to the satellite dishes possibly not being configured correctly)
- Make sure there are invisible walls for parts of the level where you don't want the player to go / climb

- There should be less visibility in the distance for the cities
- For UI, the bright thing should be the element that's highlighted
- Make the tutorials better by making them seem more like a real space. Maybe add buildings in the background or something
- We need to get proper framerate, lighting, enemy placement, and enemy behavior before we can rly get solid feedback on combat. 
- Buff the explosive mine power

### Combat1
- Remove static enemies inside the warehouse. It's confusing to have 12 enemies in front of you and the UI says "8 enemies remaining"
- The rooftop combat after the warehouse took WAYYY too long.
	- A continuous spawner does not work here. Especially if the spawn points are spread all across the multiple buildings. The player frequently has to run back and forth between the rooftops to find enemies.
	- Those small rooftops at the far left and far right sides of the area should not have melee enemies on them. Since there is a rooftop right before them, the player can just stand on the other rooftop and shoot the melee enemies with absolutely no threat.
- Change the spawners to use the wave spawner script instead of continuous
- Change the name of the "elevator keycards"
- fix the respawn points (the ones for when you fall off the level)
### Movement2

- We still need to change the direction of the wall climbs so that the player does not need to wind around the wall OR make the spaces before the wall climbs more open so that its easier for the player to get a running start.
- Z fighting on one of the roofs
- The transition to the cinematic is a bit abrupt. If it's gonna be immediate, at least make the camera transition smoothly

### Aiden Mindbreak

- Move the trigger colliders back so the player can complete the level without having to stop as they wait for the animation to play. Having to wait completely stops the flow of the game.

### Movement3

- A real problem we have is that the crane moves the shipping containers to areas offscreen. As a result, the player does not know where to go sometimes.
	- We could have a flashing light for some things to draw attention to where the cranes moved to. Or even on the crane itself.

### The Horde Mode Level
- The space itself isn't engaging enough rn
	- Add some interactable elements
	- Our game has multiple mechanics (wall running / sliding / etc.), we can play into that a little more in the combat areas so that its not just run and shoot
- We could use elevation as utility for the player
- 
