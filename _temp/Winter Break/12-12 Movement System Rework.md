The player getting caught on the floor panels is killing me.

Solution: Stop letting the player touch the ground:
<https://www.youtube.com/watch?v=qdskE8PJy6Q&ab_channel=ToyfulGames>

$${v_{nextFrame} = (force * fixedDeltaTime) + v_{currentFrame}}$$

In this equation, force serves as our acceleration and fixedDeltaTime is the variable we operate on.

Therefore, if we get the derivative of this equation, we get the following:

$${force = ???}$$

### Changes
- The player no longer get stuck on the floor panels when moving
- The player's movement is now completely physics based. Instead of immediately setting the velocity whenever the player moves, the player accelerates and decelerates based on the force applied to them.
- 

### Known Bugs
- The player does not stick to the floor properly when going down slopes too fast
-
