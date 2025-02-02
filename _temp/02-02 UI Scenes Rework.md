- [ ] Pause
- [ ] Vendor
- [ ] Tutorial
- [ ] Death

Yo ___ I wanna redo how the designers are setting up their checkpoints in their levels. Right now, the teleporter script they're using works, but each teleporter collider sends the player to a specific location and doesn't rly take into account the last "checkpoint" the player reached. This results in some weird behavior where the player falls into a teleporter collider and respawns in a location where they didn't think they would. Also, this causes the designers to miss a couple spots w/ their teleporters. I have a new idea for a system tho.

### New Checkpoint System
Basically, this system uses 2 types of colliders:
- Checkpoint colliders: When the player touches these, the script automatically stores the most recent checkpoint the player reached