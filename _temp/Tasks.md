
### Art
-

### Designer
- Create separate UI bars for the charging & cooldown meters

### Code
- Create a new power
	- Fire a projectile that explodes on contact.
	- The trajectory of the projectile should look like a grenade.
	- A reference you can use is the item "Ipecac" from The Binding of Isaac: <https://www.youtube.com/watch?v=Tr2kLXcBzDg>
	- Use the move "sludge bomb" from Pokémon Gen 6 as a reference for how it should look: <https://youtu.be/YnySK8LweUM?si=49IkFT7kBiO-x5q1&t=54>
- Create a new power #2
- Create new weapon behavior (Shotgun)
	- Follows the example set by the Pistol Prefab (Prefabs/Guns/Pistol)
	- Create a new Shotgun prefab (You can just copy / paste the Pistol prefab & change the script)
	- Replace the "GenericGun" script with a new "Shotgun" script. Make sure the Shotgun script implments the IGun interface.
	- If you want to test the gun, then you want to replace the "Initial Gun Prefab" in the player prefab with the new Shotgun prefab (The player prefab is Prefabs/AndreScenePrefabs/Player). Drag n Drop the new shotgun prefab into the "Initial Gun Prefab" slot of the WeaponManager component.

- Enemy that fires projectiles
	- Create a new enemy prefab & Add the essential scripts (Enemy & EnemyInfo)
	- Make sure this new script implements the IEnemyBehavior interface & the IDamager interface.
	- For an example, look at the "Proximity Enemy" prefab in Prefabs/Enemies/ProximityEnemy

- Enemy basic movement script
	- MUST work with NavMesh
	- NavMesh your own scene first
	- Create a new enemy prefab & Add the essential scripts (Enemy & EnemyInfo)
	- Make sure this new script implements the IEnemyBehavior interface.
	- Find a way to make the enemy navigate the scene using the NavMesh system

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
	- MUST be able to walk on the walls or something idk. I need more details.

##### Things to Do For Each Feature

#####

##### Enemies
- Enemy movement behavior
- Enemy attacking behavior
- Model
- Texture
- Animation
	- Idle
	- Move
	- Attack
	- Hurt
	- Death
- Sound
	- Idle
	- Move
	- Attack
- Any particle effects / VFX

##### Powers
- …

```cs

for (int i = 0; i < NodeList.Length; i++)
{
	int nextIndex = (i + 1) % NodeList.Length;

	Gizmos.color = Color.red;
	
}

```

