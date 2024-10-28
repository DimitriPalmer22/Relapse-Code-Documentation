The checkpoint system is composed of 2 parts: checkpoint detection and respawning

#### Checkpoint Detection

As the player progresses through each level, they will find "safe rooms". (Similar to the Resident Evil games). In these rooms, the player interacts with a burner phone. 

> NOTE: these burner phones aren't modeled yet

These burner phones act as the checkpoints.

> NOTE: the player NEEDS to interact with the burner phone to get the checkpoint

##### How the Interaction Should Work

The game already has code to handle interacting with an item by pressing 'E'. 

To use this system, the game object you want to interact with NEEDS a script on it that implements the IInteracable interface.

- If you want to see the IInteractable interface, it  is found in _Scripts > Util > Interfaces. Look in here for some comments to describe what each function is supposed to do.

Make sure you create the methods / parameters properties found in this interface.

> NOTE: you are NOT supposed to manually call these functions. The PlayerInteraction script on the player does that for you.

##### Storing the Checkpoints

The implementation of how the checkpoints are stored is up to you. It just needs to be flexible enough so that it will work with any level in the game with minimal effort from the designers. 

#### Respawning

When the player dies through normal means (health falls to 0 during combat, the player falls out of the bounds of the map, etc.) they respawn at the furthest checkpoint they reached.

When the player dies from relapsing too many times, they respawn at the beginning of the level.

For now, you can just reload the scene and set the player to move

##### Detecting When the Player Dies through Combat Vs Relapsing

I have some code in the "PlayerInfo" script found on the player that will help with this. 

You can use the OnDeath event. Inside functions you add to this event, you can check for

- When the player dies from normal means (the Damager is an Enemy / is null)
- The player dies from relapsing (The damager is the player)

These variables are found in the event args that are passed to the function.
