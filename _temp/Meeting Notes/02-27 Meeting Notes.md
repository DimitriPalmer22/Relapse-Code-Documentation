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

# Meeting notes

- Do main menu
- The current ui is the wrong type of cartoony
- We need building chunks
- Weapon balancing
- TTK is hard to gauge since there's no variability(?)
	- Missing introduces variability
		- Magazine and reload time introduces variability 
		- TTK numbers are based on NOT MISSING. So he can go in and re-tune them
	- There's also too little feedback for getting a hit
	- Sound, ui element
		- If we do a sfx, limit the sounds per second
		- Look at Halo Infinite as a reference
		- Cant tell if the shots are actually landing
		- Call of duty 
		- Apex legends
	- If we do a critical hit spot, we should do a the head
	- 1.5x multiplier
- Sound needs to be balanced. Shbeeb was getting earfucked
- Texturing
- Borderlandsy type. We needa go back and redo the textures
	- Debris + shipping container
	- If we populate Aiden's level, we should be good for the rest of the levels
- FOR NOW, we should do a gameobject / face count limit for the buildings
- Put the glowy eyes on every monster
- Make the eyes brighter as the enemy gets further away

Tuesday

- Get the whiteboxed shit out of the levels
- Seamless level transitions
- Drunkard by Tuesday
- Emissive Lighting in the level
- Put in the power effects on the hand
- We'll use the test level to show off powers
- FIX NAVMESHES IN YOUR LEVELS
- Place the enemy spawners in the apartment
