# What UI Does Our Game Need Right Now?

![](<../_META/Attachments/Pasted image 20250316150025.png>)

Right now, we have 3 bars that need to be redone:

- Health bar (Top middle)
- Stamina bar (Below the health bar)
- Toxicity meter (Bottom left)

As far as I know, our in-game UI is still supposed to be somewhat minimal. The UI isn't supposed to take up too much space on the screen.

In fact, not every single bar needs to be visible at all times (this can still change, though). For example:

- The health bar only shows up when the player's health is below 100%
- The stamina bar only shows up when the stamina is below 100%
- The toxicity meter only shows up if the players toxicity is above 0

## What Do We Want?

We want two different types of bars:

- The health bar (a unique and identifiable bar)
	- Since we're still trying to go for a minimal look, we don't want the health bar to be *too* detailed
	- The bars fade in and out, so it'd seem a little strange to have this crazy detailed health bar pop up out of nowhere
- A general bar (for stamina and toxicity)
	- These should be simpler and more generic than the health bar
	- This way, we can slap them on the screen without them looking out of place

## How Do We want Them?

### Colors

You don't need to color the bars in yourself. We can tint them in-engine.

# HI-FI RUSH

![HI-FI Rush Screenshot](<../_META/Attachments/Pasted image 20250316144542.png>)
<https://www.youtube.com/watch?v=pVtx3C5sb1o&ab_channel=GameRiot>

> Try to watch the video in the highest resolution possible because YouTube's compression makes it really hard to see the halftones on some parts of the UI.

### The Health Bar

Try not to replicate the overall shape / angle / placement of the health bar. Instead, focus on the details.

- Their health bar is too jagged
- The angle is tilted upward, which we don't really want for our game (at least I don't think we do)

If you zoom in on the health bar, you can see very subtle dots used to create a halftone effect.

### The Yellow
