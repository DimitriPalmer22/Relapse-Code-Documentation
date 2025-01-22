- [x] Wall climb when you're on the ground
- [x] Make a script for removing the gun in the tutorial
- [x] Exploding Barrell script
- [x] Reset save data when pressing play
- [x] Menu Stack (specifically for having tutorials before you enter a menu)
- [ ] Make a different layer for wall climbing vs wall running
- [x] Speed threshold when trying to wall climb from the floor
- [ ] Elevator platform script for player

### Elevator Script
- This script should work with any moving platform that uses the animator to move (not just up and down)
- The animator component NEEDS to have the "update mode" set to "Animate Physics". Otherwise, the player will not stick to the platform
- As a child of the platform that is animated, create a trigger collider that about is as wide as the platform. Move the trigger a little bit above the platform. Then, attach the "ElevatorPlatform" script to the trigger. That's it.
- If you wanna see an example, check out the "Elevator" game object in the Garden_WallRunning scene.

### Powers
- [x] Chain damage ability (chain lightning type shit)
- [ ] Spread damage / shotgun ability (imagine a bunch of small fireballs with big spread)
- [ ] Virus infliction ability (attack 1 enemy with a poison ability, killing this enemy spreads the poison to nearby enemies)
- [ ] Defensive wall (could be elemental with inflictions upon the enemy if they run into the wall. Ex, lightning wall, fire wall.
	- Lightning would stun if enemy runs into and provides cover,
	- fire would inflict burn DOT if enemy runs into it and cover)
- [ ] AOE debuff zone
- [ ] BLACKOUT - Deadass just the chain lightning power, but YOURE the thing that moves

Add more convenient button controls to the menu
Create a demonstration for the menu

Post processing

- Color temperature change to make the game look warmer
- Subtle vignette around the corners of the screen
- Subtle film grain
- Chromatic Aberration
- Lens distortion to make the center of the screen bulge away from the player
- Bloom
- Slight motion blur

Shaders

- Fullscreen Posterization shader to reduce the range of colors
- Fullscreen Halftone shader that puts dots all over the screen
- Cel shader for the enemy models

## Features to Test

Try to look for any outstanding bugs / polish issues in the following features:

- The wall-running system:
	- Running along the walls when hitting the walls with your side
	- Wall climbing when hitting the walls with your front
	- Wall jumping when pressing the jump button while on the wall
- The slide ability (c on keyboard)
- Jumping
- Guns:
	- Standard Pistol
	- Automatic Pistol
	- Hand cannon
	- Shotgun
- Enemy behavior:
	- Melee enemies
	- Ranged enemies
- Interacting with objects in the environment
- The tutorial system

### Scenes to Test in the Editor
- Garden_Ghostrunner - Test the movement & test the dash power
- Garden_CombatArena - Test all the guns & powers that are available. How does combat overall feel?
- Alex_Garden_Combat - (Turn off the Player UI game object to get rid of the images staying on screen). Test combat + test level navigation
- Mikel_GardenCombat - Test combat + test level navigation + test how it feels to have spaces with both movement and combat
- Mikel_GardenMovement - Test movement + test level navigation

# Play the Main Level in the Build
- Did the game boot up properly without any hitches?
- Is it easier to find where you need to be?
- Does the pace of the game feel slightly better?
- Does the level feel more polished?
- Are there any outstanding bugs?
- Were you able to get to the end section (the "mindbreak" area at the end)?
- Did the game feel more interesting?
- Do you think anything should be changed in this level to make the game feel more interesting?
- Was there any point of the level that felt too dark or too bright?
- Was there any point where you felt like you didn't know what was going on?

### Debug Controls:
- Comma to decrease brightness
- Period to increase brightness
- K to decrease toxicity
- L to increase toxicity
- K to take damage
- M to heal
