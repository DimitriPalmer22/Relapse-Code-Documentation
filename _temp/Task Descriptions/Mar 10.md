# Tutorial Videos

Mikel made a scene for you to record all your tutorial videos in. This way, the scenery in the videos is consistent across all the tutorials. This scene is called `TutorialVideoSandbox`.

The starting spot for each unique area for the tutorials is clearly marked with a green circle. Fly around this scene to find the starting spots for each tutorial.

> The tutorial scriptable object can be found in `Assets/Scriptable Objects/Tutorials_SO`. Make tutorial videos for everything you see here.

### Guidelines
- THE VIDEOS MUST BE IN A BUILD. A big problem we had with the last set of videos you did was that we could see the inspector / the Unity Engine window. Make a build to avoid this.
- The game should be completely full screen in the video.
- There should be no debug tools visible in the video.
- Each video should aim to convey the objective of the tutorial in 5 - 10 seconds. NO MORE THAN 10 SECONDS.
- There should be absolutely no outside software visible present in the video.
	- For instance, if you need to pull up OBS to stop recording, cut it out of the video or find some way to not have it in the video.
- Try not to have any jittery or disorienting camera movements in the gameplay
- Try not to incorporate any extraneous mechanics in a video.
	- For example, do not show any sliding in the video meant for wall running.
- If you are unsure about anything, ask.

# Create the Debug Instant Kill Weapons w/ Input for it

This is something you wanted, so this can be done to your discretion.

# Drone Shooting

- Alex's level will have *some* drones that shoot at the player.
- These drones differ from the drones that the player platforms on.
- These drones fire out of the hole that is in the front of their body.
- It is ok if the drones are stationary, HOWEVER, you can try to use the existing drone script to have the drones move around.

# Revise Power Tutorial Text

Okay, so after feedback from the CD, the tutorial text needs to go in a different direction. The text needed to be a little more instructional and less "whimsical".

- Use [POWER NAME] to [POWER ACTION] that [WHAT IT DOES TO THE ENEMIES / THE PLAYER].
- The UI in Unity recognizes *some* HTML tags, so BOLD and ITALICIZE the names of the power.
	- Surround the name of the power like `<b><i>`[POWER NAME]`</b></i>`
