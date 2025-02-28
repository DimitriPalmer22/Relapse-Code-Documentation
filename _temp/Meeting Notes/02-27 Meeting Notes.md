2-27 Shbeebism

- B to back not in main menu
- The mindbreak shader slowed down for some reason idk
- The tutorials shouldnt stop immediately, they should gradually slow down the player
- Note to self: shbeeb is a gun guy
- Auto pistol kick is lowkey is too much
- Drug names dont match graphic
- It'd be cool if we had an animation for administering the power
- It makes sense to show the FULL graphic in the vendor, but just the patch in the player's ui
- Fade to black might not be the best for the transitiosn. Maybe do a blurbor something
- The outline is cool
- Infinite mist is a cool thing, but we need a way to resolve the hard edges
- Normals in the floor textures
- Bro is still skipping stuff
- Elevator hole needs to be bigger
- That first area after ur get off the elevator is a lil dark. The player is drawn to areas of high contrast 
- Dark lightning. Makes it hard to gauge depth
- Floating buildings need to go down into the fog
- The yellow line on the draws the player to walk on the monorail. Have an obstruction or something at the end of it
- The wallrunning section felt a little close. It doesnt make sense dor some areas.

Alex combat

- The drone sound is TWEAKING.

Floor 5

- Pickup material messed up
- Phone is loud

Brian mindbrak

- No comment

Brian movement

- Lighting
- You can definitely avoid a lot of combat
- You cant kill the lesion but how would you know
- Loud glass breaking sound
- Platforms are a little tight for trying to land on if there are enemies there
- The purple seems off in relation to the rest of the area (idk if thats what he said)
- Monorail is tall type shit

Floor3

- Still some old outline effects
- Transition to aiden mindbreak broken

Aiden movement

- Color coding needs different prompting
- Red is more combat oriented
- Hitbox for shootable objects should lowkey be bigger than the actual object
- Sound effect for the crane movign would help a lot
- Bro fell through the planks
- For the ending, there needs to be some type of indication that the player needs to slide down the slope
- Scaffolding should be built in steps, not just straight up.
- For the scaffold platforming, mirrors edge is a great reference for doubling back an d knowing where to go

Floor2

- No comments

Aiden combat

- It might be better to put box collider
- Principle of level design: what is a space used for outside of a gameplay context. He said the scaffolds make no sense

- Bullet tracers could also use the comic book jitter
- In general, same side to same side jumps feel awkward

Da end

- Combat felt long and unrewarding
- Its hard to gauge how long the game is if he cant get through it
- For the level skips, we should probably make it 
- For the boomer, is it gonna be friendly fire?
- Our FOV and shit is coo
- If we do have a FOV slider, consider how the dynamic FOV contributes to that
- he likes rhe other UI, but the main menu needs to get done

For Alex warehouse, he can make it so that the crane moves into position after killing the enemies 

# 02-27 Meeting Notes

### Art

- The current UI is the wrong type of cartoony
	- The bags for the powers might not look the best in-game
	- Shbeeb suggested that we ONLY use the bags inside the shop & instead use the icons for the powers for the in-game UI.
- Our current buildings are causing performance issues (low FPS).
	- Why?: We are using too many game objects / the buildings are made up of too many faces. Even with static batching, the performance is still taking a hit.
	- Possible fix: Instead of making the buildings using models of individual blocks, we need models of "chunks" of the buildings (1 or more floors).
- Texturing
	- Borderlands type of textures. The textures need to be redone
- More props
	- If we populate Aiden's level, we *should* be good for the rest of the levels
	- We need debris / clutter
	- shipping container
### Designer

- For right now, since we don't have optimized building assets, the designers are going to have to do a bit of their own optimization.
	- FOR NOW, we should do a hard limit on the number of Game Objects AND a hard face count limit for the buildings
- The levels are too dark. Simply increasing the intensity of the directional light may not be enough.
- We need to use lights in our levels for some type of wayfinding. We can *probably* bake lights but with the way our buildings are set up, it may take too long.
	- Instead, we can use emissive materials to add light to the levels.
- Make sure the NavMeshes are rebaked before Tuesday
- Find more props / objects that could use the special jittery outline shader
- For the apartments, we can place some spawners to stop the player from just running through it.

### Other
- The game's audio needs to be balanced. Shbeeb was getting destroyed.
	- Make sure that any audio sources you're placing:
		- Are not too loud compared to the rest of the game
		- Use one of the mixer channels
- Our game's time to kill (TTK) kinda sucks because there is not much variability.
	- Conventionally, accuracy, locational damage, and stat modifiers (buffs & debuffs) add variability to the TTK
	- So, headshots WILL now be in the game and WILL now do 1.5x damage
	- This means, that TTK in our game will now be influenced by accuracy (bloom / recoil / missing shots), locational damage (headshots / critical spots), and buffs (overdrive power)
	- The TTK calculations need to factor these in

### Adding "JUICE" to the Game
- Put the glowy eyes on every monster
	- Make the eyes brighter as the enemy gets further away so they're easier to see from further away
- One reason the game's gunplay feels a little weak is because there's too little feedback for hitting an enemy. Players have a hard time telling if shots are landing.
	- Conventionally, sound and UI elements help out here
		- References, Halo Infinite, Call of duty, Apex legends
	- If we do a SFX, limit the sounds per second so the player doesn't get obliterated by the sound
	- We can do special on-screen effects whenever a critical hit (headshot) is landed

### What We Need for Tuesday

- Get the whiteboxed parts out of the levels
- Make sure the seamless level transitions work without fail
- Drunkard should be in the game by Tuesday (It's already modeled and animated). We just need to construct the prefab
- Emissive Lighting in the level so that we don't have to place & bake lights
- Put in the power effects on the hand lol
- We'll use the test level to show off powers
- FIX NAVMESHES IN YOUR LEVELS
- Place the enemy spawners in the apartment
