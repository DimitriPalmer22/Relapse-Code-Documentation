## Goal

- Get money

**Designers**:

Develop toward the 1st vendor of level 2. This includes the movement and combat areas that lead to the vendor.

> ***USE THE PREFAB VARIANTS TO SET DRESS PLEASE***
> ***USE THE PREFAB VARIANTS TO SET DRESS PLEASE***
> ***USE THE PREFAB VARIANTS TO SET DRESS PLEASE***
> This is so when / if we ever need to replace a model, we can do it in one swoop for the entire level; NOT replacing them 1 by 1.

- Implement the animations for the doctor.
- Andre, Leo, and Mikel check for level cohesion & quality of the levels.
- Leo - make sure the levels make sense in regards to Shbeeb's level design principles
- Mikel - in charge of overall level design cohesion & the overall structure of the level.
- Alex & Brian - Traversal (for now)
- Mikel & Aiden - Combat (for now)
- Enforce cohesion among the designers. We don't want extreme inconsistencies from designer to designer / area to area.
- For the traversal areas, we will actually be laying them out in relation to the level's critical path.
- For the combat areas, we are making small combat arenas. For right now, they will not be plugged into the critical path right now. We will be making combat sections and, based on how they feel, we will plug them into the level later.
- Give us a list of props you need for your levels. The artists NEED to be ahead of the designers on this. Week 1, the designers are gonna request props. By the end of the week 1, the artists should have the props done with NO TEXTURES, and should be the low poly. Week 2, the artists should have the textures done.

**Artists**:

Generally, we have what we want for a lot of the art stuff in place. WE just need to get rid of the placeholders.

> Make sure to follow the naming conventions for any models you make. You MUST follow the naming conventions.

- Modeling: Model background buildings for the level
- Animations: Redo all the enemy animations
	- Melee attack animation should NOT have the idle stances at the beginning or end
	- Walk animation needs to be an actual cycle. Also, it should not have the idle stances at the beginning or end.
	- We need a death animation (fall backward. the animation would need to make sense for pistols AND shotguns)
	- Actually animate reloading the gun
- Textures: Establish a style for the textures and convey how to do the textures to the artists.
- VFX: More VFX for the game.
	- Explosion VFX (for the power)
- Enemies:
	- Retopologize the big guy
	- Retopologize the muscular guy
- Bullet hole image

**Programmers**:

- Refine the movement system
	- Wall-climbing
	- Smoother wall-running
		- [x] Bigger angle to start wall-running
		- [x] Restrict the player from looking too far away from / into the wall while wall-running
		- [ ] If you jump while too close to the wall, you immediately wall-run. Fix this by requiring the player's movement to be directed toward the wall.
		- [ ] If you go into a wall at the wrong angle, you should not be able to wall-run.
		- [x] Sometimes the camera tilts the wrong way
- Charging enemy
- More powers
- Revisit the power sounds entirely
	- Having a one-shot sounds for charging the power is not gonna work. We need a looping SFX for charging the power and a one-shot for releasing the power. We don't think the sound for this right now fits.
	- We also need a different sound for when a power is done cooling down. We don't think the sound for this right now fits.
- Also, we need to replace the placeholder sounds for:
	- shooting
	- reloading
	- player getting hit
	- enemy getting hit
- Also, we need some more sounds for the enemies to give them life
	- Idle groaning / breathing sounds
	- A sound for when the enemy is alerted of the player's presence. Like a grunt.
	- A swipe / wind sound effect for when the enemy attacks
	- A grunt for when the enemy attacks

### Week 1

### Week 2

# Concept Graph For the Apartment

The features the player learns as they traverse the level.

- Basic Movement (walking)
- Urge Mechanic
	- Lead the player to the gun
- Interacting w/ objects
- Enemies
	- How the enemies move
	- How the enemies detect the player (Find a way to convey this)
	- Enemies have health & take damage
	- Enemies attack the player
- Shooting
	- Ammo (Find a way to convey this)
	- Reloading
- Vendors
	- Get Items from the shop
		- You can only pick one per vendor
	- Dialogue
- Powers
	- Charging the power (charge duration and stuff)
	- Releasing the power to activate it
	- The effect that activates as soon as the player releases the power
	- The power's active effect (if it has one) (How do we tell the player if the player has an active effect?)
	- The power's passive effect (if it has one) (How do we tell the player if the player has an passive effect?)
	- Break down the anatomy of a power
	- How to use whichever power the player buys
	- Toxicity meter
- Vendor 2
	- Differentiate between doctors and dealers (convey to the player that these are completely different)
	- Once the player gets the new power, they are able to switch powers.
- Heavy Enemy
	- How to differentiate them from the other enemies
	- How to damage them
	- How they attack & move
- Mindbreak section
	- WTF is a Mindbreak (We can do more to convey to the player that this is a fractured state of mind area. Maybe a visual thing.)
- Wall Running
	- The player can wall run on their left or right side
	- The player can sprint while wall running
	- The player can jump off the wall
	- The player can slide down the wall

# Concept Graph For the Next Level

The new features the player encounters as they traverse the level.

- Crawler Enemy
- Moving platforms (Make sure not to have unjustified floating platforms)
- "Breakable" items
	- Shoot at specific parts of the environment to break them & have things happen
- Sliding
	- How short is the player when they slide and what can they slide down?
	- How fast is the player is when they slide?
	- Slide cancelling (jump cancel & sprint cancel)
