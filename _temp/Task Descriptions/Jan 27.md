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

### Scenes

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

[Refresher for making powers](<../../Documentation/Powers/Powers.md>)

### Overview
- The player fires X physical projectiles, each having its own forward direction
- The direction each fireball goes should be completely random each time the power is used
- These projectiles should be about half the size of the fireball projectiles
- You could probably even copy the fireball projectile prefab and just make it smaller. Then use that prefab for the power

### Configurable Values in Editor
- Damage: the amount of damage each projectile does
- Projectile Count: the number of projectiles that are fired at once
- Any other values you think would be necessary. You might even want to check the fireball power for any values that would be good to have.

## Virus Infection Power

This is another projectile-based power, so it should not be too different code-wise from the fireball power.

[Refresher for making powers](<../../Documentation/Powers/Powers.md>)

### Overview
- The player fires a physical projectile.
- Once the projectile hits an enemy, the enemy is "infected" for a short period of time.
- While "infected", the enemy will take damage over time.
	- Use a coroutine to do this
	- To be more specific, the "infection" will tick X times. Whenever a tick happens, the enemy will take Y damage. The "infection" will tick every Z seconds.
	- So, the total damage the enemy takes is X * Y over the course of X * Z seconds.
- The projectile should be slightly slower than the fireball projectile
- The projectile should also be slightly larger than the fireball projectile

### Configurable Values in Editor
- Damage: the amount of damage each projectile does initially.
- Damage Per Tick: the total amount of damage the enemy takes while infected
- Time Between Ticks: the time between each tick
- Total Ticks: the total number of ticks the enemy takes
- Any other values you think would be necessary. You might even want to check the fireball power for any values that would be good to have.

## Go through the Game for Things that Need VFX

As you play the game, look for any features / mechanics / powers that need more visual feedback for the player to understand what is going on. Make a list and send it in the Discord
