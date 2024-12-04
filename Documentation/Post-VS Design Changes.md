# Art

We are changing the art style.

## Contemporary References

- Any telltale game for shading
- NFS Unbound for (VFX specifically)
- Borderlands for linework and textures

### VFX
- Think NFS Unbound
- 2D graphic novel / comic art
- Think speech bubbles, impact effects, etc.
- For tooltips, we can have the regular tooltips be basic speech bubbles. For the tooltips that relate to objectives, we can have them be the spiky speech bubbles.
	- NOTE: These will be animated. The speech bubbles themselves WILL NOT BE ANIMATED / WE ARE NOT USING VIDEO / GIF FILES FOR THESE.
	- Instead, the bubbles will be separated into 2 different layers for foreground and background. The background will stay stationary, but the foreground PNG will be animated via the Unity animator.
- We need 2D VFX for using the powers.

## New ART Workflow

We don't have an actual new workflow solidified right not, but we're planning to have specific people only work on specific things.
	For example, 1 person for texturing, 1 for hard-surface modeling

> [!Important]
> NO MORE HI-POLYS. It makes everything slower for the design team. Also, If you're gonna do a high to low poly, keep the naming convention the same.

### NAMING CONVENTIONS

Make sure the names are consistent

ObjectTypePrefix_AssetName_Iteration

- For example, the first version of a texture called RoofTiles would be named like: *Tex_RoofTiles_01*.
	- The only exception to this would be the bones of a rigged character.

| Object Type     | Prefix |
| --------------- | ------ |
| Texture         | Txtr   |
| Low Poly Model  | LowP   |
| High Poly Model | HigP   |
| Animation       | Anim   |

# Mechanics

## Weapons / Guns

We have to revisit what we want each gun to do for the player. As of right now, they all do the same thing: Shoot and kill the monster.

We want each weapon to define a playstyle:

- Pistol: Accurate, low damage
	- More methodical playstyle. The player needs to be more precise with their shots.
- SMG: Fast fire rate, low damage, low accuracy, really really good for short range damage.
	- More run-and-gun playstyle. The player needs to be more aggressive with their shots & has to be constantly aggressive with the enemies to use it effectively.
- Shotgun: Knockback, high damage. Less range than the pistol, but more than the SMG.
	- More of a defensive playstyle. The player needs to be more strategic with their shots. We want the enemies to come towards you with the shotgun vs. actively seeking them out with the SMG.

With all this said, though, we know the player is going to play how they want. These are just how we are intending the design to be.

The player has the opportunity to get a new weapon in each level.

- The player can only have 1 weapon at a time.
- The player is forced to pick up the pistol in the 1st level.
- In the second level, the SMG is introduced and they have the option to pick it up.
- The third level has the shotgun.
- In the 2nd and 3rd level, we will have areas where the player can choose to use a previous weapon.
	- Maybe include this as a part of the dealer's shop? It makes sense for a dealer to have weapons.

## Powers

The powers need to be much more dynamic in how the player uses them to play the game. As of right now, they're kinda just there. I forget about them sometimes I'm ngl. We need to find a way to make the player rely on powers more.

-

## Movement

- Revisit how far you can wall-run for.
	- The gravity is too strong right now
- Add juice somewhere
- SFX, VFX

## Enemies

# Designers

## New Workflow

Before we even start the favelas, we need to create some sort of test level that reflects how we want the real level to play.

- For instance, if we want a variety of wall-running and dashing sections, the test level should reflect that.
- This is done so we know the design intentions from the beginning.

Restrict the creative freedom when it comes to individual areas between the levels.

- Periodic level revision to keep things coherent and cohesive.

Maintain a staggered schedule between the lead designer and the rest of the designers. Mikel is gonna be like a week ahead in terms of the work that needs to be done for level so that he can lead by example.

- This, paired the regular check-ins, will help keep the team on track.

***USE THE PREFAB VARIANTS TO SET DRESS PLEASE***
***USE THE PREFAB VARIANTS TO SET DRESS PLEASE***
***USE THE PREFAB VARIANTS TO SET DRESS PLEASE***
***USE THE PREFAB VARIANTS TO SET DRESS PLEASE***
***USE THE PREFAB VARIANTS TO SET DRESS PLEASE***

- Mikel had to manually replace like 150 game objects because they used the FBX file and not the prefab variants.

Be careful of nesting things too many game objects into each other. This WILL cause performance issues if done too much.

- Instead, organize the hierarchy by the type of objects.
- For example, use an empty game object called "Props" and then put all the props under there (not as a child, but literally under it)

## What even is a Level Fr

- We need areas in the levels that cater to the game's mechanics. Fuck ludonarrative dissonance
- For example, we NEED arena sections where the player NEEDS to fight the enemies with their guns and powers to progress.

> [!Important]
> With the way the narrative is rn, Kin (the player) is currently remembering their past actions. So, the part of the game that you are playing is all in his head. We can use this to be more abstract with the level design & design intentions. For example, we can have fog that blocks off certain areas of the level

# Juice

## Visual

### 2D VFX
- 2D Animated tooltips
- 2D Animated power effects
	- When using the power
	- When a power comes into contact with a surface of game object
- 2D Animated muzzle flash effects
- 2D Animated bullet hit effects
	- Maybe some blood splatter?
- Any screen overlays
	- Low health screen overlay

### Animations
-
## Auditory
-
