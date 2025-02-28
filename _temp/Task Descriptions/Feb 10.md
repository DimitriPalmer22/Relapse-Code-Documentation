## Playtest the Game
- Same playtest notes as usual

## Set up a Tab System for the Settings Menu

- From now on, you will need edit the settings menu in the scene called "PauseUIScene" to edit the pause menu. Changes made here will be reflected in the rest of the game.
- Each button in the header of the settings menu should have its own separate page in the settings menu.
- Don't worry about having controller compatibility for this portion of the menu yet. It's buggy and I'm working on a fix for it.
- The current sliders for controller / mouse sensitivity should be moved to the "Controls" tab of the settings menu. Also, it should be noted that these sliders are placeholders that will eventually be replaced. Maybe don't use these as one-to-one references for the other tasks.
- The rest of the tabs do not need to be populated yet. They are placeholders for future settings that will be added to the game.

## Setting for Brightness / Gamma in the Menu

- This setting will be a simple slider that controls the brightness setting in the game.
	- Make this slider go from -1 to 1.
- This slider will go in the "Video" tab of the settings menu.
- The code / behavior for the brightness setting in the game already exists. We just need a UI element in the settings menu that changes it.
- This setting exists in the `UserSettings` script. To change the brightness, you can call the `SetGamma(float value)` function in this script.

### Connecting the Slider and the Brightness Setting

- I recommend adding a new script to the slider.
- In this new script, make a function called `ChangeGamma(float value)` or something like that.
	- Inside this function, call `UserSettings.Instance.SetGamma(value)`.
- On the slider component, drag the slider script you just made into the "On Value Changed" event. Then, assign the `ChangeGamma` function to this event.
	- Doing this will make it so that when the slider is moved, the brightness setting in the game will change.
- For polish, I recommend that in the start function of this script, you set the slider's value to the current brightness setting in the game.

## Settings for Audio Settings in the Menu

- This task will most likely take you the most time out of all your tasks for this week.
- For this task, you are allowed to edit the `UserSettings` file, and you are encouraged to do so.
- The settings for this task will go in the "Audio" tab of the settings menu.
- The volume for the audio in our game uses the audio mixer in Unity. The audio mixer is a powerful tool that allows us to group and control the volume of all the audio in the game.
- Look up "AudioMixer" in the assets folder and you'll find the asset for the audio mixer.
- Our audio mixer has 7 tracks:
	- Master
	- Music
	- Game Sfx
		- Player
		- Enemies
		- Other
	- UI Sfx
- Each track has a volume setting that can be controlled.
- Your job is to create sliders in the settings menu that control the volume for each of these tracks.
	- There is *NOT* existing code for this in the `UserSettings` file. You will need to create this code.

![](<../../_META/Attachments/Pasted image 20250210182636.png>)

- Re-check GPU instancing
- Material complexity
- Colliders
- Reconsider the back-faces of the building blocks