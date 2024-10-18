
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

1. First, the enemy behavior script needs to extend the `MonoBehaviour` class to be added to a game object.
2. Next, the enemy behavior script needs to implement the `IEnemyBehavior` interface. As of right now, this interface has no methods. It is just a marker interface to show that the script is an enemy behavior script.
3. From here, you can do whatever you want for the enemy's logic.

#### Doing Damage to the Player

If your script does not do damage to the player, you can skip this.

If you want the enemy to be able to damage the player, you can implement the `IDamager` interface.

Your class's definition should look like:

```csharp
public class YourClassName : MonoBehaviour, IEnemyBehavior, IDamager
{
    // Your code here
}
```

This interface includes 1 property:

```csharp
public GameObject GameObject { get; }
```

This property should be replaced with:

```csharp
public GameObject GameObject => gameObject;
```

Now that this is set up, you can now work on the damage logic.

To do damage to another entity, that entity NEEDS a script that implements the `IActor` interface.

- For the player, that is the `PlayerInfo` script.
- For enemies, that is the `EnemyInfo` script.

