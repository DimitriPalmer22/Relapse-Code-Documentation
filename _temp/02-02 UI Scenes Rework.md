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

### Overview

Basically, this system uses 2 types of colliders:

- Checkpoint colliders: When the player touches these, the script automatically stores the most recent checkpoint the player reached.
- Reset colliders: When the player touches these, the script will reset the player's position AND ROTATION to the *most recent* checkpoint they crossed. This way, the designers can just put big ass reset colliders everywhere to make sure that the player can never get out of the level. Also, the designers don't have to specify respawn positions for every single collider they place.

### How to Use

- ***FOR THE LOVE OF GOD, PLEASE PUT ALL OF YOUR TRIGGER COLLIDERS ON THE "NonPhysical" L***