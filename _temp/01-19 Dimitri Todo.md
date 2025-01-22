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
- The wall-running system:
	- Running along the walls when hitting the walls with your side
	- Wall climbing when hitting the walls with your front
	- Wall jumping when pressing the jump button while on the wall
- The slide ability
- Jumping
- Guns:
	- Standard Pistol
	- Automatic Pistol
	- Hand cannon
	- Shotgun

### Scenes to test in the Editor
- NAB_PlayerData
- Garden_Ghostrunner

# Play the level in the build
