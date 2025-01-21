- [x] Wall climb when you're on the ground
- [x] Make a script for removing the gun in the tutorial
- [x] Exploding Barrell script
- [x] Reset save data when pressing play
- [x] Menu Stack (specifically for having tutorials before you enter a menu)
- [ ] Make a different layer for wall climbing vs wall running
- [x] Speed threshold when trying to wall climb from the floor
- [ ] Elevator platform script for player

### Elevator Script
- This script should work with any moving platform that uses the animator to move (not just up and down)
- The animator component NEEDS to have the "update mode" set to "Animate Physics". Otherwise, the player will not stick to the platform
- As a child of the platform that is animated, create a trigger collider that about is as wide as the platform. Move the trigger a little bit above the platform. Then, attach the "ElevatorPlatform" script to the trigger. That's it.
- If you wanna see an example, check out the "Elevator" game object in the Garden_WallRunning scene.

### Powers
-  
