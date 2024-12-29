
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
- [ ] Support for multiple interactable scripts on 1 object
- [ ] More responsive button input for menus
	- [ ] Back button / menu stack support for ALL menus (use abstract methods)
	- [ ] Im ngl i need to make another input action for UI
- [ ] Instead of having menus pop up, have them fade in and out.
- [ ] Also, transition menus to having an active flag in them
- [ ] Black screen overlay for when
	- [x] the player dies
	- [ ] the player respawns
- [ ] Some type of death animation / ragdoll
- [ ] Disable player controls when dying
- [ ] Shake screen while relapsing

###### UI
- [ ] Charge Meter on UI
- [ ] Cooldown Meter on UI (Make panel darker or something)
- [ ] Find a solution for showing power names on UI. Make a prefab that holds a TMP_Text object w/ the desired text on it. Instantiate this / copy its settings over whenever a power is selected
- [ ] Support for different types of tooltips (they'll use different prefabs)
	- [ ] Objective
		- [ ] New Objective
		- [ ] Objective Complete
	- [ ] Money
	- [ ] Tutorial
	- [ ] General Information
	- [ ] Debug
###### Keeping Player Information between States
- [ ] Store the player's information into a more serializable format (have a class or a struct or something for each important component of the player)
- [ ] Whenever a scene is loaded, have a script check to see if an instance of this data exists. If so, apply it to the player. Otherwise, keep the player's data as is.
- [ ] When the player wants to SAVE the game, this script gets serialized
- [x] Also, fix the loading in the apartment scene

###### Sound

<https://www.youtube.com/watch?v=DU7cgVsU2rM&ab_channel=SasquatchBStudios>

- [x] Sound Mixing
- [x] Might have to completely remove the sound manager script
- [x] Instead, have several audio sources on the player that play specific sounds. This way, I can control which sounds are playing at any given time and which audio source they play from
- [ ] Play sound when enemies are damaged
- [ ] General enemy sounds to give them life (growls and stuff)
- [ ] Play sound when player is damaged
- [ ] Play sound when enemy dies
