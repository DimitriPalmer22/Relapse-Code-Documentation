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

![](<../_META/Attachments/Pasted image 20250316152032.png>)

Also, we need a large comic-y text box asset for the game's longer dialogue. It should roughly be the same size as the image above.

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

***You don't need to color the bars in yourself. We can tint them in-engine. In fact, we'd prefer if you sent us the bars in black-and-white / greyscale so its easier to tint in-engine.***

Each bar is going to be 1 color. However, a gradient from black to that color is fine.

> If you want to put a gradient on the bar, then you can use a gradient from black to white when making the asset. In-engine, we can then tint the bar from black to the color of the bar.

### Placement

The toxicity meter is going to remain in the same spot.

However, you can experiment with moving the health & stamina bars to different locations on the screen.

- You can keep them in the top middle if you want
- Or you can move them to the top left
- The top-right is being used for tooltips, so we can't put them there
- The bottom right *might* be too out of the way

### Shape and Style

When making the bars, try to make the actual image as horizontal as possible, we can rotate them in-engine to get the look you want.

The bars should be simple and clean. We don't want them to be too detailed. They should be very easy to read at a glance considering the player needs to be able to see them while in combat / moving around the level.

# HI-FI RUSH

![HI-FI Rush Screenshot](<../_META/Attachments/Pasted image 20250316144542.png>)
<https://www.youtube.com/watch?v=pVtx3C5sb1o&ab_channel=GameRiot>

> Try to watch the video in the highest resolution possible because YouTube's compression makes it really hard to see the halftones on some parts of the UI.

### The Health Bar

Try not to replicate the overall shape / angle / placement of the health bar. Instead, focus on the details.

- Their health bar is too jagged
- The angle is tilted upward. This works for them since their UI is in the top corner of the screen.

If you zoom in on the health bar, you can see very subtle dots used to create a halftone effect.

If the halftone effect is too much, we can ***try*** to replicate this effect using shaders in-engine.

### The Yellow Comic Bubble

I'm not sure if we need a bubble like this, but this is a good example of the overall shape of the comic bubbles we want.

Also, they have this halftone shadow behind the bubble. If we want to replicate this, make the shadow a separate asset / image file. This way, w This way, we can easily change the shadow's color in-engine.

