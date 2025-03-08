[02-27 Meeting Notes](<./Meeting Notes/02-27 Meeting Notes.md>)

# Firearm

The boss is gonna use the standard pistol. However, we need a clear and easy way to telegraph that the enemy is about to shoot. We also need to make sure it is easy enough for the player to dodge the enemy attack.

- Honestly, using the existing code in the Shooting attack script might suffice. Like the enforcer / lesion ranged enemies, we can use an animation event to show that the enemy is shooting.

# Neuro / Vital Powers

I need a centralized way to easily add boss logic to EACH power.

Boss Power SO

- Corresponding Player Power
- Charging
	- Move while charging
	-

# Extra Abilities

One thing I'm worried about is the boss not being very engaging if the player chooses not to take any Neuros. So, I propose an extra system to keep the fight interesting.

- The boss ALSO has 3 power up abilities equipped (Like overdrive)
- Based on the phase the boss is currently in, the enemy gains an extra ability.
- Each ability is also indicated by an outline material (with its own unique color)
- At the start of the boss fight, they're all disabled.
- At the start of each phase (after the initial phase), a new power-up ability is "unlocked"
	- Every couple of seconds, the boss will choose one of the "unlocked" abilities and temporarily turn it on
