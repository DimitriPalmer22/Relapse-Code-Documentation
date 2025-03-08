[Based on this video](https://youtu.be/-Ts9xF9Owe0?si=4c4MbWk_C0yvd2iy&t=492)

- Determining how to attack / move is determine by 1 BRAIN script
- The brain checks a series of variables to determine the different *behavior States*

DECOUPLE:

- Movement & Detection behaviors. Movement script should only control moving from point to point. The brain of the enemy determines which function to run.
- New movement script: Contains all the code possible for walking to a given point, strafing, or wandering.
	- Each movement state has its own corresponding update function
- The old movement scripts will be used as additional logic for if a specific movement state should be implemented

### Behavior State
- A set of conditions (To determine if the state)
- A set of Things the enemy can do:
	- Attack
		- Attack number (to play a specific animation)
		- Weight (for random change)
	- Movement Action
		- Weight
		- Cooldown Range (How long it should do the action for )

- FIELDS
	- Time since last seen target
	- Number of other enemies nearby

BRAIN

- Check for which behavior state to go in
	- Single Behavior State
		- Conditions
		- Attack Action
		- Movement Action
	- Behavior Substate Holder
		- Conditions
		- Single Behavior State OR Behavior Substate Holder
