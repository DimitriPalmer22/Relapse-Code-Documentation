The player getting caught on the floor panels is killing me.

Solution: Stop letting the player touch the ground:
<https://www.youtube.com/watch?v=qdskE8PJy6Q&ab_channel=ToyfulGames>

$${v_{nextFrame} = (force * fixedDeltaTime) + v_{currentFrame}}$$

In this equation, force serves as our acceleration and fixedDeltaTime is the variable we operate on.

Therefore, if we get the derivative of this equation, we get the following:

$${force = ???}$$

## Changes
- The player's movement is now completely physics based.
- Instead of immediately setting the velocity whenever the player moves, the player accelerates and decelerates based on the force applied to them.

### Basic Movement
- The player no longer gets stuck on the floor panels when moving

### Wall Running is no Longer Buttcheeks
- The player can no longer wall run backwards
- The player will automatically fall off the wall if they are not moving fast enough
- The player will not stick to walls if they are not fast enough
- When the player starts wall running, they preserve some of the momentum they had before wall running
- The player gradually falls down the wall as they wall run
- Wall jumping force and angle have been adjusted slightly
- The player can now properly sprint while wall running

## The Short-Ranged Dash is Better
- The player can now dash up ramps / stairs

## Known Bugs
- The player does not stick to the floor properly when going down slopes too fast
- Jumping as the player lands can sometimes make the player jump higher than usual
- I'm pretty sure I fixed this, but there *was* a bug where dashing on probuilder slopes would cause the player to no-clip and fall into the slope
