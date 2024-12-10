1. New black outline shader around pretty much everything
2. New fullscreen shader that puts dots in dark areas of the screen to give a halftone effect
3. Implemented a new asynchronous level loading system that only loads parts of the level at a time & DRASTICALLY increases performance
	- Remade the apartment level using this system & it works!
4. Made new lighting settings that result in smaller & lower-res light maps.
	- Baked the remade apartment scenes + the LobbyFavela scene w/ these settings
5. Made a new post-processing volume & applied it to the remade apartment scenes + the LobbyFavela scene
6. Increased compression on EACH of the environmental textures in the game
	- this cut the build size in half after I also made the light maps lower res
7. 
