Based on [this video](https://www.youtube.com/watch?v=raQ3iHhE_Kk&ab_channel=Unity)

# Engineering Pillars
## Modular

- Systems are not directly dependent on each other

> EXAMPLE
> Let's say I have an inventory system in my game. I want that to communicate with other systems in my game, but I don't want a hard reference between them. This makes things less flexible and I can't reassemble things in cool ways.

### Scenes as Clean Slates
- No transient data between scenes
- Minimize objects that use "Don't destroy on load"
- This allows for scenes that have unique behavior that is not present in other scenes
- You want prefabs that work on their own. (Don't rely on other prefabs)
	- Helps with source control in larger teams.
	- Helps with modularity

> IN SUMMARY
> Scenes are just a list of prefabs. Prefabs are the individual functionality.

### Components
- Break things up into components that do 1 thing and only 1 thing.
## Editable (At runtime)
- Focus on data-driven design.
- Our game is data. Our systems are machines that process this data.
- Change the game without changing code.
- This allows for *emergent design*: Designers can make things without having to ask for a specific feature. We can make new game mechanics we didn't even know existed.
- The more we can change the game at runtime, the more we can fine-tune and experiment with values. If we can save our runtime-state (like how we can with scriptable objects), then great!

## Debuggable
- Test any single piece in isolation
- The more editability we have, the more we can have debug views and features.
- Never consider some feature done until you have some plan for how you're going to debug it.

# Scriptable Object Basics
- Serializable data container class
- saved as .asset files OR can be instantiated at runtime without an asset
	- Also, you can save multiple instances of a scriptable object into a single asset file.

## Simple Use Cases
- Game config file
- Inventory
- Enemy Stats
- 