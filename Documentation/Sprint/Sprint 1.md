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

1. The player spawns inside a bedroom and is let outside into the hallway. Immediately their path to the right is blocked, so they progress down the path to their left until they find themself at a crossroads. The player turns right towards the brightly lit path and ignores the dark hallway on the left. They continue down the brightly lit path until they enter an open room with a gun on the table. The player picks up the gun, unlocking their first weapon, and continues through the room, passing through a hole in the wall that leads them to another bedroom.
2. The player exits this bedroom and continues towards the brightly lit elevator lobby on their right. From the elevator lobby, the player has 3 different hallways to choose from, the most inviting being the one on the right. The player progresses down the right hallway and turns into another brightly lit room on the right-hand side, which leads them to another hole in the wall. Through this hole in the wall the player enters the final room, in which they walk out into a new hallway and see the exit stairwell down the hall on their left, which then brings them up to the 5th floor.
3. Players enter the 5th floor from the top staircase of the level. As the player enters the 5th floor, they go to the left, progressing through the room with the hole in the wall. From the green exit sign the player sees once they get out of the room, the player needs to move forward until they reach the 2nd right turn. The player needs to take this right turn and stay on this path all the way until they reach the left turn that feeds the player into a room with the light on outside. Once players enter this room, they interact with the dealer to get their first power. Once they get a power, the player exits the room to the right and follows the path until they reach the staircase.
4. Players use this staircase to descend from the 5th floor to the 3rd floor. 
5. From the stairwell, players turn right and continue down a bright hallway. Players are drawn to a room which has a hole in the wall which leads to a set of pipes. Players navigate on the pipes reaching another room which they enter via a hole in the wall. From this room, players exit through a door reaching another bright hallway to the right. While moving forward down this hallway, players come across an open doorway next to a bright door light. Entering this room, players are led to another hole in the wall, leading to a hallway with a maintenance closet.
6. The maintenance closet cannot be entered due to wooden boards. Realizing entrance to the closet is not possible, players enter another room via hole in the wall parallel to the previous hole. Exiting the room through a doorway, players enter a large lobby area with multiple elevators. Players notice a flickering light above a keycard panel, prompting them to interact with it. Interacting with the keycard panel does nothing. Players notice a bright hallway next to the elevators. Players navigate down this hallway and come to two paths. Players turn left and then right down this path.
7. Players enter another long hallway and turn right towards the bright lights. Moving straight, players come across another room with a flickering light. A crowbar is laying on a table in the room, and the players grab it. Players then back track through the level towards the wooden boards. Players use the crowbar on the wooden boards, making the maintenance room accessible. In the room, a keycard is located on the table, which the players grab. With the keycard, players traverse back to the keycard panel in the lobby area. The keycard activates the keycard panel, opening an elevator door. Players then enter the elevator to find a hatch. Players enter the hatch.
8.	The player exits the elevator into a hallway with three paths. One path is blocked off, one path is dark, one path is brightly lit with an exit sign. The player walks towards the exit sign. Before the player gets to the exits sign, an enemy bursts through the wall and blocks their path.
9.	The player turns around to see that a door behind them is open. They walk into the room and find a checkpoint. They then progress out the door and through the next hallway, they may need to hide in a room as a monster walks by. They turn left at the end of the hallway to see an open door. They enter and meet a dealer. They heal and regain their ability to sprint and jump. They progress back to the previous checkpoint through a one-way passage. They walk out through the door at the other end of the room where they are chased by the same monster that broke through the wall earlier. They reach a hole in the floor that they must jump over (if they go this way before finding the dealer they will be unable to make the jump, they will land in a maintenance shaft and walk back to the checkpoint area, or be killed by the monster). The player runs to the stairwell and exits the floor
10.	The player exits the stairwell and walks to the end of an empty hallway, reaching an opening into the apartment lobby, a spacious area riddled with monsters. The player frantically combats the monsters to make their way to the front of the lobby, where the exit of the building lies.