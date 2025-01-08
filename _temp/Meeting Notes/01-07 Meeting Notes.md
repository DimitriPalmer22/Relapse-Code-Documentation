# 01-07 Meeting Notes

@everyone PLEASE REPLY TO THIS MESSAGE TO CONFIRM THAT YOU'VE SEEN IT.

Here are some notes from the meeting we had after Shbeeb ended class early on 01-07:

## General Stuff
- Sprints are going to be Monday - Sunday
- Our sprints are 2 weeks long.
- Halfway through each sprint, everyone's respective lead(s) will check in on them to see how they're doing. This is to catch problems before they happen / determine if we need to reduce the game's scope for some reason.
- The gameplay / aesthetic of the level we showed in Vertial Slice DOES NOT fully represent how we want the game to be. The game from this point on will be much faster paced.

## The Gauntlet / The UI
- The game will NO LONGER have a completely diegetic UI through the gauntlet on the player's left hand. In fact, the gauntlet might not even be a gauntlet anymore.
- In fact, the entire idea / design of the "device" on the player's left hand.
- Alex & Azalee are in charge of concepting new looks for it.
	- *HOWEVER*, we still need to pin down how exactly we want the "device" / left arm to be animated while the player is using a power.
- From now on, we will have a more traditional minimal UI.
- Any diegetic UI that is a part of the "device" on the player's left hand will purely be there to supplement the traditional UI.

### Why Are We Getting Rid of the Gauntlet???
- If you look at almost any FPS game, the player's hands are directly in front of the screen. This is because this is the most natural position to hold a gun in. However, in our game, we would need to pose the hands awkwardly no matter what in order to show off any UI on the player's left hand.
- If the player's left hand gets animated at any point, the diegetic UI on the arm becomes infinitely harder to read. Also, any pose / animation we do for the hands has to account for the player seeing the UI.
- There's too much information we want to convey to the player for it all to fit on the UI. Instead of completely reworking the UI, it'd be easier to just make a more traditional UI.

## The Hands
- The hands will be repositioned to hold the player's weapon more conventionally.
- Any time the player uses a power, the left hand will be animated to move away from the gun.

## Art Style
- We are leaning heavily into the more comic book aesthetic for the game.
- To do this, we are implementing 2D effects in a lot of places to spice up the game visually.

## Animations
- The animations for the enemies that are currently in the game need to be reworked.
- Andre will be in touch to describe how the animations should be done.

## Level Design
- From now on, the game's levels need to properly account for the game's mechanics.
- To do this, we are splitting the next level into 2 different sets of sections: Movement sections and Combat Sections.
- This way, we can more concretely focus on how we want the player to play the game in specific environments.

## Problems with the Game

One of the biggest problems we have is conveyance: when people play our game, they often have no idea wtf is going on.

- Players had a hard time understanding what exactly the powers did.
- Players couldn't really differentiate between drug-based powers and med-based powers.
	- On top of that, players didn't really understand the repercussions of using the drug-based powers over the med-based powers.

### How to Fix Them

- Unique particle effects for the different powers in the game. This way, the player can easily tell what power they just used. This also plays into the whole aesthetic of the player tripping balls.
- More proper tutorialization. Whenever the player encounters a new feature / mechanic / power, the game will pause and a tutorial screen will pop up with a video + text description of how to use the new thing.
	- The player *should* also be able to access these tutorials from the pause menu.
	- We want something like this to avoid incorporating the tutorials into the levels themselves.
- To differentiate the drug-based powers from the med-based powers, we *could* have different icons for both. For example, the drug-based powers could have a skull icon while the med-based powers could have a green cross icon or something.
	- Additionally, we *could* have separate animations for when a drug is used vs. when a med is used.
-
