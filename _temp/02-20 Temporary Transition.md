We need transitions since the cutscenes don't work.

- Repurpose those "checkpoint resets" that move the player to the next level.
- Make a new script with pretty much the same structure, but uses a coroutine to
	- disable player movement / damage,
	- fade the screen to black,
	- THEN move the player,
	- and then fade from black
