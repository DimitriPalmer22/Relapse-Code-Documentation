
> [!NOTE]
> We are calling those black and white transition zones "Mindbreaks".

# The Gameplay Loop?
- GRIMWAR: Move really fast while wall-running and jumping. Use powers to navigate the levels / fight enemies. Over and over and over.
- Veilwood: Farm during the day, fight during the night. Get money, go to town.
- Relapse: 1. Use powers, 2. Use weapons, 3. Use movement.
	- Use powers and weapons while dynamically moving to kill enemies. Decide which power to use: drug or meds.
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
- Enemy death poof VFX. We need to have a poof of smoke when the enemies die.

### Player Animations
- We are completely scrapping each hand operating independently. It looks too awkward.
	- There's no way to naturally do this while showing the UI at the same time.
- Use both hands to hold the gun por favor.
- The left hand will transition from the gun to the power charge animation when the player uses the power.
	- The left hand animations will keep the palm facing up so that the diegetic UI will still be on-screen
- Remove the syringe from the top side of the player's hand. Having something hang from an appendage is a little weird.
- Instead, near the elbow (remember, the palm is facing upward), we will have all 4(?) power vials to indicate which powers the player currently has equipped.
	- The vials drain when the player uses the power.
	- As a matter of fact, we need to redo the syringe images Robert made. The player is NOT using syringes for the powers. The gauntlet uses vials to administer the powers.
	- Also, we need to have some type of tube to convey that the tubes are draining into the player's system.
- We need to add a camera shake for when the player gets hit.
- Right now we have no way to convey to the player how charged the power is.
	- When the player is actively charging the power, they'll have one animation. Maybe like an open hand. The hand is open, but tense.
	- When the power is fully charged, the player will have a closed fist. It should also shake a lil bit.
	- When the player uses the power, they will release their clenched fist.
	- Keep in mind, the palm is still facing upward in all these motions so that the UI is still visible.
- We are now gonna use both hands to reload. Powers are disabled while reloading.
- Gun recoil animation
- While the player is relapsing, shake the left hand.

### Common Enemy Animations
- Each of these animations is going to be found on every enemy, no matter how the behave.
- Idle animation LOOP. it has to seamlessly loop
- Walking LOOP. it has to seamlessly loop
- Running LOOP. it has to seamlessly loop
- Hurt / flinch animation. DOES NOT need to loop

### Specific Enemy Animations
- For each enemy model, we need to explicitly define EXACTLY how we it to attack.
	- We may want to reuse models for the sake of different enemy variations.

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

| Object Type     | Suffix |
| --------------- | ------ |
| Low Poly Model  | _low   |
| High Poly Model | _high  |
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

## Powers (Kinesis)

List of kinetic powers: <https://powerlisting.fandom.com/wiki/List_of_Kinetic_Abilities>

The powers need to be much more dynamic in how the player uses them to play the game. As of right now, they're kinda just there. I forget about them sometimes I'm ngl. We need to find a way to make the player rely on powers more.

### Power Ideas
- For NOW, we are deciding to categorize powers based on the type of kinesis they apply to. For example, pyrokinesis, telekinesis, etc.
- A power like Wraith in apex legends. We disappear for a short time and reappear somewhere else.
- Blink like Dishonored or that one guy in [Valorant](<#Valorant>)
- Put down a mine
	- Regular fire mine
	- Gravity mine - When enemies activate the mine, every enemy within a certain spherical range gets sucked in
- [Záriakinesis](https://powerlisting.fandom.com/wiki/Dice_Manipulation "Dice Manipulation")
	- Dice rolling power
	- 2D VFX could be rolling die
	- Activate any one of the random powers
	- Random change to activate a bad power that is exclusive to the random power.
		- This can be the explosion power. It does damage to the player and the enemies
- Gun-Kinesis
	- Drug
	- You shoot a fucking gun
	- One tap an enemy or some shit idk
- Rate of fire increase
	- Med
- Aurakinesis
	- Change an enemy's aura so that other enemies see it as an enemy temporarily
- Kamikaze-Kinesis
	- When the power is fully charged, the player will zoom forward for about 3 seconds
	- When the power is released, release an explosion that:
		- deals a little bit damage
		- knocks the player backwards IN THE DIRECTION THEY ARE FACING
			- So if they are pointed downward, the explosion will send them straight up.

### Vendor
- The vendors will carry more powers.
- The player is still GUARANTEED 1 power from each vendor.
- Half of the vendor's powers will be free.
- The other half are the really good powers that require money to buy.
- Regardless of if you get a free power or a paid power, you can only get ONE power per vendor.

#### Memories
- Memories will give money on pickup to encourage exploration

### Toxicity & Relapse
- Bigger tolerance meter / more drugs until relapse
- when you relapse, both hands tweak out for 5 secs.
	- you cant use a gun or powers
- 3 RELAPSES WILL NO LONGER KILLS YOU
- Immediate effect of a Relapse: the maximum value for the toxicity meter goes down by like 10%. This value persists between levels.
	- The player cannot lose more than 50% of their max tolerance in each level.
	- When they end the level, they regen half of the max tolerance they lost during the level.
- Level-to-level effect: The maximum health value of the player goes down by 5% for each time you Relapse in that level up to a maximum of like 80%

[Toxicity Revamp.excalidraw](<../_META/Excalidraw/Toxicity Revamp.excalidraw.png>)

## Movement

- Revisit how far you can wall-run for.
	- The gravity is too strong right now
- Add juice somewhere
- SFX, VFX

## Enemies

Enemies can be defined by two components: movement behavior & attacking behavior.

### Movement Behavior

- Patrolling
- Stationary (dont move at all)
- Guards (won't move until they see the player)
- Enemies with a front shield that can only be attacked from behind. They'll constantly reposition to face the player.

- Flying Enemies that chase the player

### Attack Behavior
- Melee - Play melee attack animation
- Ranged - Fire a projectile at the player w/ a shooting animation
- AOE - Play an AOE animation
- Charge - Play the sprint animation & run toward the player

### Enemy Placement
- Enemies need to be placed in a way that forces the player to use their mechanics (movement + gun + powers)
- Combat needs to be engaging and challenging
- Introduce the enemies and their mechanics in a way that the player can learn how to fight them. Then, ramp up the difficulty. Then, mix them together.
	- Half Life 2 did this well apparently
	- We'll have a small arena with 1 enemy in it. That enemy will have further range than normal so that the player can learn how to recognize the enemy and how to fight it.
	- We can also have a small arena with a few of the new enemy in it.
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

## What Even is a Level Fr

- We need areas in the levels that cater to the game's mechanics. Fuck ludonarrative dissonance
	- Movement mechanics that we want the player to use
	- Shaping the level to reinforce combat / the desired gameplay loop.
- For example, we NEED arena sections where the player NEEDS to fight the enemies with their guns and powers to progress.

> [!Important]
> With the way the narrative is, Kin (the player) is currently remembering their past actions. So, the part of the game that you are playing is all in their head. We can use this to be more abstract with the level design & design intentions. For example, we can have fog that blocks off certain areas of the level until we kill enough enemies to progress.

- We need more areas that play into this abstract / surreal reality concept. We need the player to feel more like they are tripping balls.
	- The apartment level is based too much in reality.
- Our levels need to focus on verticality & our movement system

- Vendors can be placed in hidden areas.
	- These hidden vendors will *ONLY* have paid powers.
	- The dialogue for these vendors need to imply that they are not tied to the character's backstory. Therefore, they will NOT give the player free drugs!
# Juice

## Visual

### 2D VFX
- 2D Animated tooltips
- 2D Animated power effects
	- When using the power. Different effects for each power
		- Think [Fragpunk](<#Fragpunk>)
	- When a power comes into contact with a surface of game object
- 2D Animated muzzle flash effects
- 2D Animated bullet hit effects
	- Maybe some blood splatter?
- Any screen overlays
	- Low health screen overlay
	- When we enter a Mindbreak, play a wobbly screen overlay effect

Also, de-load the surrounding scene so it seems kinda trippy.

### Dynamic Post-Processing VFX
- Chromatic Aberration heartbeat effect for the Mindbreak sections

## Auditory
-

# Contemporaries

Literally every hero shooter.

## Fragpunk
- Hollowpoint's ability in Fragpunk is a good example of what we want the power VFX to look like.
## Valorant
- <https://www.youtube.com/watch?v=0s97LxpDz48&ab_channel=DiamondLobbyValorant>

- <https://discussions.unity.com/t/graphic-novel-style-shader/847955>
- <https://discussions.unity.com/t/comic-book-shader/691128>
- <https://www.youtube.com/watch?v=xAdB3OxpC7Y&ab_channel=GameDevGuide>
- <https://www.google.com/search?q=unity+graphic+novel+art+style&oq=unity+graphic+novel+art+style&gs_lcrp=EgZjaHJvbWUyBggAEEUYOTIHCAEQIRiPAjIHCAIQIRiPAtIBCDMyNThqMGoxqAIAsAIA&sourceid=chrome&ie=UTF-8>
- <https://community.telltale.com/discussion/57236/how-to-draw-telltale-games-style>
- <https://www.reddit.com/r/Unity3D/comments/12qhbfg/how_can_i_make_a_3d_game_look_2d_in_the_style_of/>
- <https://www.google.com/search?q=borderlands+art+style+in+unity&sca_esv=22db317853775bed&ei=m7FTZ73yFZbIwN4Pn_rmoAM&ved=0ahUKEwj9q8OGzZSKAxUWJNAFHR-9GTQQ4dUDCA8&uact=5&oq=borderlands+art+style+in+unity&gs_lp=Egxnd3Mtd2l6LXNlcnAiHmJvcmRlcmxhbmRzIGFydCBzdHlsZSBpbiB1bml0eTIFECEYoAEyBRAhGKABMgUQIRigATIFECEYoAEyBRAhGKABMgUQIRifBUj7G1AAWJsbcAB4AJABAJgBeqAB8ROqAQQyNi40uAEDyAEA-AEBmAIeoALbFMICCxAuGIAEGJECGIoFwgIREC4YgAQYkQIY0QMYxwEYigXCAgsQABiABBixAxiDAcICERAuGIAEGLEDGIMBGNQCGIoFwgIREC4YgAQYsQMY0QMYgwEYxwHCAggQABiABBixA8ICCxAuGIAEGLEDGNQCwgIaEC4YgAQYkQIYigUYlwUY3AQY3gQY4ATYAQHCAg0QLhiABBhDGNQCGIoFwgILEAAYgAQYkQIYigXCAgoQLhiABBhDGIoFwgIKEAAYgAQYQxiKBcICHBAuGIAEGEMY1AIYigUYlwUY3AQY3gQY4ATYAQHCAhAQLhiABBixAxhDGNQCGIoFwgINEC4YgAQYsQMYQxiKBcICCBAuGIAEGLEDwgILEC4YgAQYsQMYgwHCAgUQABiABMICBRAuGIAEwgIGEAAYFhgewgILEAAYgAQYhgMYigXCAggQABiABBiiBMICCBAAGKIEGIkFwgIFECEYqwKYAwC6BgYIARABGBSSBwQyNS41oAfXvwI&sclient=gws-wiz-serp>
- <https://www.youtube.com/watch?v=9dIyEUpsb1Q>
- <https://www.youtube.com/watch?v=3iZrZrEWQuA&ab_channel=DanielIlett>
- <https://www.reddit.com/r/comicbooks/comments/sqh5e9/simulating_original_paper_colour_and_texture_for/>
- <https://www.reddit.com/r/Unity2D/comments/13ham78/unity_fullscreen_shader_graphs/>
- <https://i.sstatic.net/PADZw.jpg>
- <https://www.youtube.com/watch?v=JBpxSQrZRXg&ab_channel=MichaelsGameLab>
- <https://www.youtube.com/watch?v=mNpC6nB4uFM&ab_channel=GabrielAguiarProd>
- <https://www.reddit.com/r/Unity3D/comments/pom3ju/how_to_make_my_lighting_more_or_less_similar_to/#lightbox>
-
