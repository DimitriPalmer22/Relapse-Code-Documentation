Based on [this video](https://www.youtube.com/watch?v=raQ3iHhE_Kk&ab_channel=Unity)

# Engineering Pillars
## Modular

- Systems are not directly dependent on each other

> EXAMPLE
> Let's say I have an inventory system in my game. I want that to communicate with other systems in my game, but I don't want a hard reference between them. This makes things less flexible and I can't reassemble things in cool ways.

### Scenes as Clean Slates
- No transient data between scenes
- Minimize objects that use "Don't destroy on load"
- This allows for scenes that have unique behavior that is not present in other scebes
## Editable (At runtime)
## Debuggable
