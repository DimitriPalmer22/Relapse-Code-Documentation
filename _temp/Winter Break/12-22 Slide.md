# Slide Mechanic

### Using the Slide
- Use ctrl / circle to slide
- The player can slide while they are moving on the ground
- The player can also press the slide button up to half a second before landing to initiate a slide (this was to make the jump slide feel more responsive)
	- This number can be changed in the inspector
- When walking / running into a slide, a constant force added to the player at the start of the slide to push them forward
	- This constant force can be changed in the inspector
- When jumping into a slide, the slide script takes into consideration the player's y velocity as they land and proportionally adds a force to push the player forward.
	- The amount of velocity preserved can be changed in the inspector
	- The maximum amount of force transferred can also be changed in the inspector
- The player will automatically stop sliding once their velocity falls below a certain amount
	- This number can be changed in the inspector
- Press the slide button again to stop sliding
- You can also jump directly out of a slide
	- Jumping out of a slide slightly preserves your momentum for a short time, so you can jump -> slide -> jump to move around faster
- NOTE: the slide pushes the player in the direction they are already going, NOT the direction they are facing. So, they can theoretically be looking / shooting left while sliding right

### Bugs / Things to Be Added
- Sliding down slopes does not continuously accelerate the player slide yet
- The player does not get shorter when sliding yet
- Other things idk
