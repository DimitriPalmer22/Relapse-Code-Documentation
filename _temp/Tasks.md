
#### Art
-

#### Designer
- Create separate UI bars for the charging & cooldown meters

#### Code
- Create a new power
- Create a new power #2
- Create new weapon behavior (Shotgun)
	- Follows the example set by the Pistol Prefab (Prefabs/Guns/Pistol)
		- 
	- You do not need to create a new model or anything, literally just copy the current gun prefab & make a new script for it

- Enemy that fires projectiles
	- Create a new enemy prefab & Add the essential scripts
	- Make sure this new script implements the IDamager interface

- Enemy basic movement script
	- MUST work with NavMesh
	- NavMesh your own scene first
	- Find a way to make the enemy navigate the scene

- Completely re-design a new movement system so it completely relies on changing the rigid body's velocity (This removes jank) (Dimitri)
	- Input Mapping
	- Basic WASD Movement on the ground
	- Sprinting
	- Jump
	- Short-range Dash
	- Wall Running
	- Wall Jumping
	- Climbing

- Advanced enemy movement script
