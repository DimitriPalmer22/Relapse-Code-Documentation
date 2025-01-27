- Playtesting: Most of the same notes for playtesting as last time still apply

## Playtesting

Try to look for any outstanding bugs / polish issues in the following features:

- The wall-running system:
	- Any hiccups with the wall running that make the game feel janky
	- Is the player randomly falling off the walls / is it hard to initially stick to a wall?
- The slide ability (c on keyboard)
- Jumping
- Guns:
- Enemy behavior:
	- Melee enemies
	- Ranged enemies
- Interacting with objects in the environment
- The tutorial system

### Scenes to Test in the Editor

You *should* also be able to access these scenes from the main menu. So, you can choose to build the game before you play or play in-editor.

Note: the names of the levels in the editor don't match the names of the levels in the menu.

- Aiden_Garden - Test the level overall. How is movement + combat + the progression of the level?
- Garden_Ghostrunner - Test the movement & test the dash power
- Garden_CombatArena - Test all the guns & powers that are available. How does combat overall feel?
- Alex_Garden_Combat - (Turn off the Player UI game object to get rid of the images staying on screen). Test combat + test level navigation
- Mikel_GardenCombat - Test combat + test level navigation + test how it feels to have spaces with both movement and combat
- Mikel_GardenMovement - Test movement + test level navigation

### Play the Main Level in the Build

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

### Debug Controls

- Comma to decrease brightness
- Period to increase brightness
- K to decrease toxicity
- L to increase toxicity
- K to take damage
- N to take a little damage
- M to heal

## Spread Damage / Shotgun Power

This is another projectile-based power, so it should not be too different code-wise from the fireball power.

### Overview
- The player fires X physical projectiles, each having its own forward direction
- 

### Configurable values in Editor
- Damage: the amount of damage each projectile does