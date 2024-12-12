# Changes I've Made So Far
1. Added a cel shader to the enemies
2. New black outline shader around pretty much everything
3. New fullscreen shader that puts dots in dark areas of the screen to give a halftone effect
4. Implemented a new asynchronous level loading system that only loads parts of the level at a time & DRASTICALLY increases performance
	- Remade the apartment level using this system & it works!
5. Made new lighting settings that result in smaller & lower-res light maps.
	- Baked the remade apartment scenes + the LobbyFavela scene w/ these settings
	- We should be using these settings to bake for our weekly builds, NOT the high quality settings we've been using
6. Made a new post-processing volume & applied it to the remade apartment scenes + the LobbyFavela scene
7. Increased compression on EACH of the environmental textures in the game
	- this cut the build size in half after I also made the light maps lower res
8. Added fog
9. Increased the gravity in the physics menu so the player feels WAYYYYYYY less floaty now.
	- Once I get all the movement mechanics working fully again & make a little test scene for it, the player's movement should feel much more tight
10. Also increased the base speed of the player a teeny bit

# Things I Plan to Do (In no Particular order)

### Movement
- In general, I want to increase the pace of play, so I will change the current movement system to reflect that.
- Fix the wall-running
- Fix going up & down slopes
- Do cool visual effects when moving
	- FOV change when sprinting

### Enemies
- Fix the jank for the currently existing enemies
	- Fix their navmesh stuff
	- Fix how easy they are to go around / get out of sight
	- Fix how easy it is to get out of range of their attacks
	- Make them move faster / make them an actual threat for the player
	- Use animation events to control when the enemy's hitboxes become active
- Make new enemy types
	- At least 1 type of enemy that is medium / long ranged.
	- I want to make these so we can know how to build the favelas around them

### Powers
- Create some of the powers that were written down in [Post-VS Design Changes](<../../Documentation/Post-VS Design Changes.md>)
	- More meds need to be made for sure.
	- At least one of the meds needs to be a movement power or something. People are getting the wrong idea that the meds are just buffs / heals
- Add a charge meter or something to the UI to convey to the player how charged their current power is
- Implement the new mechanics for the Toxicity Meter & Relapsing

### Test Level
- A test level needs to be made.
- This level will be representative of how we want combat / movement / overall pace of play to feel in the rest of the game.
- Open combat areas:
	- Big enough to use the movement mechanics
	- walls to run on
	- platforms to jump on
	- enough enemies so the player can get overwhelmed & they NEED to use some type of power

### Polish / Other Stuff
- Add a flinch or something when getting hit & remove that debugging tooltip whenever the player takes damage

### Bug Fixes
- [ ] Controls don't disable while in menus
- [ ] If you get a checkpoint on one part of the level & unload that part of the level, the player will respawn at the checkpoint but the level will still be unloaded
- [x] Add the main menu back to the game
- [x] Clicking the start button twice on the main menu loads the game twice
- [ ] Fix that one "Relapsed!" screen bug that locks the game
- [x] Fireball not hitting enemies in the lobby
- [ ] Other bugs idk
