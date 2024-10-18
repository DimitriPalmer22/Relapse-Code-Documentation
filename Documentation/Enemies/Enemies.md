
***WIP***

### Creating an Enemy

> If you want to see an example of how to create an enemy, look at the "Proximity Enemy" prefab in the `Prefabs/Enemies` folder.

Each enemy prefab needs to have the following components:

- The "Enemy" script found in the `_Scripts/Enemies` folder
- The "EnemyInfo" script found in the `_Scripts/Enemies` folder
- A new script that implements the `IEnemyBehavior` interface

The "Enemy" script just holds references to the EnemyInfo script and the script that implements the IEnemyBehavior interface. *This script does not need to be edited, just drag and drop it onto the enemy*.

The "EnemyInfo" script holds information about the enemy's health and handles the logic for when the enemy takes damage. *This script does not need to be edited, just drag and drop it onto the enemy* (It should be added automatically when you add the "Enemy" script).

The script the implements the `IEnemyBehavior` interface is where you will write the logic for how the enemy moves / attacks. This script should be added to the enemy prefab as well. *This is where you write your code*.

### Creating an Enemy Behavior Script
