
- [x] Dash as a power
- [x] Fix jumping on slopes
- [x] Stop wall jumping as soon as you touch a wall
- [x] All dynamic cam effects not working in build
- [x] Grab an enemy's attention when shooting them
- [x] Player controller spring feels too squishy in the apartment level because THE ENTIRE THING IS SLANTED. So, have the slope fix be proportional to the slope of the surface
- [x] Enemies have different speed for unaware & aware states
- [x] Find some way to convey invincible state to the player
- [x] Script to control the PP volume so I can add dynamic PP effects
	- [x] Add a vignette that shows up when the power is done charging
- [x] Fix enemy sliding as much as I can
- [x] Ranged Enemy
- [x] Replace animator for muzzle flash w/ a visual effect graph
- [x] Time scale manager
- [x] Hard speed limit
- [x] Prefire the jump (Make it override the slide & vice versa)
- [x] Bullet hole code
- [x] Bullet trail code

###### Movement
- [ ] ~Slide down slopes
- [ ] ~Variable jump height
- [ ] Fix the wall running
	- [ ] only the left and right rays detect if the player is wall running or not right now
	- [ ] Make wall-running less sensitive. Make it so that the player's velocity has to be going into the wall somewhat for the player to wall-run (use dot product & angles)

- [x] Consolidate pistol & shotgun scripts
- [ ] ~~Enemy tinting~~ Visual Effects for enemy status effects
- [x] Visual Effects for when enemies are hit
- [x] Visual Effects / indication for when powers are done charging
	- [ ] Different VFX for each power
- [ ] More enemy abilities
- [ ] ~~Support for multiple interactable scripts on 1 object~~
- [ ] More responsive button input for menus
	- [x] Back button
	- [ ] menu stack support for ALL menus (use abstract methods)
	- [ ] Im ngl i need to make another input action for UI
- [x] Instead of having menus pop up, have them fade in and out.
- [ ] Also, transition menus to having an active flag in them
- [ ] Black screen overlay for when
	- [x] the player dies
	- [ ] the player respawns
- [ ] Some type of death animation / ragdoll
- [ ] Disable player controls when dying
- [x] Shake screen while relapsing
- [ ] When the player is done relapsing, stop the overlay image from disappearing instantly. Use a lerp to make it fade out
- [x] Dynamically increase chromatic aberration when the player is relapsing / they have relapsed more than once on the level

###### UI
- [ ] Charge Meter on UI
- [ ] Cooldown Meter on UI (Make panel darker or something)
- [ ] Find a solution for showing power names on UI. Make a prefab that holds a TMP_Text object w/ the desired text on it. Instantiate this / copy its settings over whenever a power is selected
- [ ] Support for different types of tooltips (they'll use different prefabs)
	- [ ] Objective
		- [ ] New Objective
		- [ ] Objective Complete
	- [ ] Tutorial
	- [ ] General Information
	- [ ] Debug
- [x] World space UI element for displaying selected item text. (instead of just basic text on the screen)
- [x] Dynamic reticle support (Change the icon based on what the player is looking at)
###### Keeping Player Information between States
- [ ] Store the player's information into a more serializable format (have a class or a struct or something for each important component of the player)
- [ ] Whenever a scene is loaded, have a script check to see if an instance of this data exists. If so, apply it to the player. Otherwise, keep the player's data as is.
- [ ] When the player wants to SAVE the game, this script gets serialized
- [x] Also, fix the loading in the apartment scene
- [ ] Serializing the scene: each level should have a script with a list of bools that represent the state of the level. When the player saves the game, this list gets serialized and saved to a file. When the player loads the game, the list gets deserialized and the level is set up based on the state of the list.
	- [ ] This still doesn't account for enemies, but I have an idea. Make it so that in the Enemy class, each enemy has a specific ID. When the player saves the game, the list of enemies in the level is serialized. When the player loads the game, the list of enemies is deserialized and each enemy is spawned in based on the ID of the enemy. This way, the player can save the game and come back to the level with all the enemies they killed still dead.

###### Sound

<https://www.youtube.com/watch?v=DU7cgVsU2rM&ab_channel=SasquatchBStudios>

- [x] Sound Mixing
- [x] Might have to completely remove the sound manager script
- [x] Instead, have several audio sources on the player that play specific sounds. This way, I can control which sounds are playing at any given time and which audio source they play from
- [x] Play sound when enemies are damaged
- [x] Play sound when enemy dies
- [ ] General enemy sounds to give them life (growls and stuff)
- [x] Play sound when player is damaged

###### Guns
- [x] Buy guns
	- [x] Put a cost field in the scriptable object
	- [x] Make a game object (like an item frame in Minecraft) that holds the gun prefab. When the player interacts with this object, they can buy the gun
- [x] Scriptable objects for gun variations
- [x] Prefabs for gun variations

TODO: 12-30

- [x] Guns Buying and selling

TODO: 12-31

- [x] The rest of guns
- [x] Dynamic reticle support (Add a cursor type getter in the interactable interface)
- [x] Make interface for objects that should be saved and loaded
- [ ] Make a level script to set up keeping the player's information between levels.

<https://www.youtube.com/watch?v=gqtin0F3ejI&ab_channel=WishboneGames>

Alright I played it for a while and here's my feedback:

### Difficulty
- Right now, I think the arena feels a little too hard. And no, I'm not just bad at the game. Here are some possible fixes
	- The guns need to be more powerful
	- The melee enemies need to be a *teeny* bit slower
	- There need to be less enemies altogether
	- The enemies need to do less damage
- Whichever one of these we choose (if we do choose one), we have to make sure the rest of the game still feels good after the change. We wouldn't want the apartment level to feel too easy cuz of something we do here.

### Movement & Architecture
- I like the way the level is built. Visually, it is obvious that the player is about to enter a combat space.

### Things that need to be fixed / changed
