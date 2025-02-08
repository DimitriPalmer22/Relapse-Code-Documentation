
# Continuous Enemy Spawner

The script is called "ContinousEnemySpawner"

This script randomly spawns different enemy prefabs at random locations.

### When Do Enemies Spawn?
You have the choice of: 
- having enemies spawn as soon as the game starts (this isn't recommended because the ) 
- manually starting and stopping the spawner externally.

### How Many Enemies Are Spawned
- There is a value for controlling how many enemies are active at once (its called "Max Active Enemies") so the player doesn't get too overwhelmed
- The spawner can spawn enemies infinitely or until a certain number of enemies are spawned

### Extra Functionality
- There is a Unity Event that gets called whenever ANY enemy dies. Idk what you can use this for, but its there.
- There is a Unity Event that gets called whenever all the enemies in the spawner are defeated (if the spawner is not infinite). You can use this to open a door or something after the player kills all the enemies

### Example

You can see an example of this script in the "Garden_EnemySpawners" scene.

Under the "Spawner Area 1" object, there is a game object called "SPAWNING", which contains the script.
