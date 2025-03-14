
- Sound curation is going to be your focus for this week. The game is going to be given more life via sound.
1. Revisit the power sounds entirely
	- Having a one-shot sounds for charging the power is not gonna work. We don't think the sound for this right now fits.
	- Instead, we will have a looping sound effect when the player is charging their power.
		- This way, the player can charge their power for an indefinite amount of time and the sound effect will loop.
		- This sound effect NEEDS to be uninvasive and subtle so that player won't get annoyed any time they charge a power.
	- Then, once the player releases the power, we will have a one-shot sound effect for that.
	- We also need a different sound for when a power is done cooling down. We don't think the sound for this right now fits.
2. Also, we need to replace the placeholder sounds for:
	- shooting
	- reloading
	- player getting hit
	- enemies getting hit
3. Also, we need some more sounds for the enemies to give them life
	- Idle groaning / breathing sounds
	- A sound for when the enemy is alerted of the player's presence. Like a grunt.
	- A swipe / wind sound effect for when the enemy attacks
	- A grunt for when the enemy attacks

> The code does not exist yet for some of these. DO NOT WORRY ABOUT IMPLEMENTING THESE SOUNDS. Just find them / ask your sound person to create them. From there, we will look at the sounds you've gathered and determine if they fit the game's aesthetic.

---

The menus in our game don't really feel good when trying to navigate using buttons (on a controller or even a keyboard).

- In an empty scene, create a simple menu system that feels good to navigate with a keyboard AND controller. The menu doesn't have to do anything, but should be functional in terms of navigation and interacting with elements
- The menu does not need to be pretty, but it should be blatantly obvious what everything on-screen is.
- The menu should look like the following:

![](<../../_META/Excalidraw/01-09 New Menu Specifications.excalidraw.png>)

![](https://static.wikia.nocookie.net/temtem_gamepedia_en/images/f/f1/SettingsGame.png/revision/latest?cb=20201002182857)

Based on these images, the menu should have:

- A header with
	- 4 buttons in it that span across the top of the screen. I suggest you use a [Horizontal Layout Group](https://docs.unity3d.com/Packages/com.unity.ugui@1.0/manual/script-HorizontalLayoutGroup.html) for this.
	- These buttons represent which page of the menu the player is currently on. The player can navigate to different pages by selecting a button.
	- The selected page's button NEEDS to remain highlighted for as long as the player stays on the page.
- Multiple pages, with each clearly having its own subset of elements
- UI Elements
	- Simple buttons.
		- These should work with the 'submit' button (Enter on keyboard, A on XB1 controller, X on PS4 controller)
	- Value pickers.
		- These are buttons that increment / decrement a value when the player interacts with them. For example, the player can use these to change the volume of the game.
		- When the player presses / holds left or right on a value picker, the value should increment / decrement.
	- Checkboxes
		- These should work with the 'submit' button (Enter on keyboard, A on XB1 controller, X on PS4 controller)
		- Pressing the submit button should toggle the checkbox's state between on and off
	- It might help to organize the UI elements using a [vertical layout group](https://docs.unity3d.com/Packages/com.unity.ugui@1.0/manual/script-VerticalLayoutGroup.html).
- A functional scrollbar.
	- This should work with the mouse wheel, and should also work with a controller's joystick.
	- Also, the scrollbar should reset whenever the player navigates to a new page
