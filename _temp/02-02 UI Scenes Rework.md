- [ ] Pause
- [ ] Vendor
- [ ] Tutorial
- [ ] Death

Yo ___ I wanna redo how the designers are setting up their checkpoints in their levels. Right now, the teleporter script they're using works, but each teleporter collider sends the player to a specific location and doesn't rly take into account the last "checkpoint" the player reached. This results in some weird behavior where the player falls into a teleporter collider and respawns in a location where they didn't think they would. Also, this causes the designers to miss a couple spots w/ their teleporters. I have a new idea for a system tho.

### New Checkpoint System

Basically, this system uses 2 types of colliders:

- Checkpoint colliders: When the player touches these, the script automatically stores the most recent checkpoint the player reached.
- Reset colliders: When the player touches these, the script will reset the player's position to the *most recent* checkpoint they crossed. This way, the designers can just put big ass reset colliders everywhere to make sure that the player can never get out of the level. Also, the designers wouldn't have to specify respawn positions for every single collider they place.
The only downside for this is the fact that the designers would have to redo their colliders for their levels.

# New Checkpoint System

The current system you guys have been using for when the player falls of the level is a placeholder. I have made a new system to replace it / make it better.

You can see examples of this new system in:

- The Garden_WallRunning scene under the CHECKPOINTING object
- The Garden_Ghostrunner scene under the "CHECKPOINTING (NEW)" object

## Overview

Basically, this system uses 2 types of colliders:

- Checkpoint colliders: When the player touches these, the script automatically stores the most recent checkpoint the player reached.
- Reset colliders: When the player touches these, the script will reset the player's position AND ROTATION to the *most recent* checkpoint they crossed. This way, the designers can just put big ass reset colliders everywhere to make sure that the player can never get out of the level. Also, the designers don't have to specify respawn positions for every single collider they place.

## How to Use

### Creating a Checkpoint Collider
1. To create a checkpoint collider, create a new game object w/ a trigger collider on it.
2. Then, put the "LevelCheckpointCheckpoint" script on it.
3. This script needs a transform that the player will respawn at. You can just drag the game object into this slot, OR you can use some other game object if you want
4. Then, you need to adjust the box collider's bounds to make it easier for the player to walk through the collider while playing the game.
5. Since this new system will respawn the player facing a specific direction, you may to adjust the rotation. To do this, you can either adjust the y-rotation of the respawn point OR change the "rotation" value in the "LevelCheckpointCheckpoint" component.
6. The green ball gizmo shows you where the player will respawn at. The red arrow gizmo above that shows you which direction the player will be facing when they respawn.

- ***FOR THE LOVE OF GOD, PLEASE PUT ALL OF YOUR TRIGGER COLLIDERS ON THE "NonPhysical" LAYER***

### Creating a Reset Collider
- Create a trigger collider
- Put the "LevelCheckpointReset" script on it
- Adjust the collider how you please

- ***FOR THE LOVE OF GOD, PLEASE PUT ALL OF YOUR TRIGGER COLLIDERS ON THE "NonPhysical" LAYER***

## If Your Level Has the OLD System in it

You do not need to completely delete your old checkpoints if you don't want to. You can transfer these to the new system by:

1. Select ALL of the colliders with the old "Teleporter" script on them
	- If you want to search for every object in the scene with the Teleporter script on it, look up "t: Teleporter" (without the quotes) in the hierarchy.
2. Disable / Delete the Teleporter script on these objects.
3. Add the "LevelCheckpointReset" script to them

That's it! You successfully converted these to reset colliders.

*YOU STILL NEED TO MAKE THE CHECKPOINT COLLIDERS MANUALLY, THOUGH*
