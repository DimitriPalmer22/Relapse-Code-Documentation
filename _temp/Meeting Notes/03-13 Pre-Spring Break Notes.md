# 03-13 Pre-Spring Break Notes
- Game too long
- We STILL need to add more combat
- The apartments need to be condensed somehow

- Brian's movement needs to be shortened
	- It may be a good idea to end the level after breaking the glass

## Boss Fight
- The boss fight is too dense & has too much going on with it

### No Court Room Arena
- Having a section where the player fights in the courtroom feels a little busy
- The courtroom can be used for a cutscene
- Move the courtroom cutscene to the end

### MIKEL IDEA: FOR THE VOID SCENE IN BRIAN'S LEVEL
- Orb has 3 positions.
- INSTEAD of just going through the void, the orb leads you through the different floors of the apartments.
	- The orb leads you on where to go, BUT you can turn around and explore the apartments if you want.
- Also, we're playing this scene BEFORE the boss fight btw.
- This works cuz the orb is the boss
- This is an actual intro to the boss

## Combat
- Enforcer has 100 health so he is the basis for all the enemies
- Lesion is slightly healthier
- Drunkard has the most health.
- Crawler has the least.

- Enemies will become more difficult in each level.

- How do we convey that the player is in a space where they can't continue without killing all enemies?
	- Leo's dissolve shader. It'll fade in as you enter the space and fade out as you leave / clear it.
	- Also, some type of visual motif to signal the area

- How many enemies are left?
	- Show a tooltip in the top right to show how many enemies are left in the spawner

#### Extra Gamemode
- Hoard mode
- Special game mode where the player fights waves of enemies.
- Keep going forever.

## Motifs for Mindbreak Areas
- Post processing change
- Background music ambience in the areas
- Mindbreak splotches as decals or something
- Dissolve shader for enemy wave spaces

## Journal

Get rid of the journal as-is

- Converting the pause menu into the journal
- Objectives are not present in the rest of the level and are lowkey not needed
- Inventory - Just showed in the main menu
- Powers - Just show in the main menu
- Memories are too high-scope, so we no longer need them hoes
- Show the numeric value for health and toxicity values in the pause menu AND the upgrade menu for the vendors

## VFX
- Spawn VFX for enemies so that they don't just pop in
	- Mindbreak VFX effect
- We need grayscale versions of Alex's VFX animations so we can spam them everywhere
- Use the exclamation point / lightning as a VFX so that points of interests are easier to see

## Sound
- We NEED sound effects for everything in the game
- The new enemies need new sounds
- The enemy groan gotta go
- The animations NEED sounds to go along with them
- Footsteps
	- Floor
	- Wall running
	- etc.
- Slide
- Shotgun blast SFX

# Absolutely Changing the Apartments
- THIS DOES NOT APPLY TO ALEX'S FLOOR since its pretty much in-line with what we want anyway

### The Idea
- The apartment levels are used PURELY for:
	- getting a power from the vendor
	- Getting Dialogue / Lore

### Pathing
- The critical pathing of the apartments NEEDS to be shortened a little.
	- *Like Deadass turn the path after the vendor room into a hallway*
- The player starts in the vendor room
- The player CANNOT exit the dealer room because the door is locked. They NEED to get a power to unlock this door. (interacting with the door gives you a tooltip or something)
- However, the player can still EXPLORE the apartments to keep the space interesting
- At the end of the critical path, have "Nega" Kin visible at the end of the critical path.
	- Have a light shining on him
	- Have a SFX accompanying him
	- For right now, have him poof away and leave behind an explosion VFX
	- (POST-ALPHA) Have the dissolve thing around the player's camera instead of a fade to and from white

### Visuals
- Dense mindbreak splotches along the critical path
- Mindbreak splotches along the critical path will become more dense for each apartment level. I.E. floor 4 has the least. Floor 2 has the most
- Parts of the apartment that aren't along the critical path will have little-to-no splotches

### Lore
- Forced to walk in the distressed hallways. This way we can make sure we deliver the story
-

# Vendor Rework
- Eliminate the idea of "Doctors" and "Dealers"
- The vendors are now just "a guy". They have different names
- Each dealer will have an increasing selection of powers, which allows you to get the powers that you missed before
- Power tutorials inside the vendor UI so the player knows how the powers work BEFORE they buy it
- When buying NEUROS ONLY, have a have a confirmation saying "are you sure you want to buy this?" to provide additional hinting for not buying neuros
