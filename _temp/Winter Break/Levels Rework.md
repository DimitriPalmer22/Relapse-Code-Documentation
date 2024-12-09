# Changing the way We Do the Game's Levels

The way we've been doing levels is completely WRONG WRONG WRONG. Although it helped with Git management, that whole prefab system thing caused us more problems than it solved.

- Unnecessarily large prefab files
- Long saving times when making changes to a level prefab
- Things being overridden in the ApartmentBlockout scene, but not the scene the designer was working in.
- "Bro, who touched my prefab?"
- etc.

## From Now On, Each Level is Going to Be Split up into Multiple Scenes
### Why Do This?
- This is high key how you're supposed to handle large and complex levels.
- A large level can be broken up into smaller, more manageable scenes. This makes performance in the editor itself better and allows for collaboration between level designers. This also allows for proper asynchronous level loading
- Unity can have multiple scenes open at once in the editor.
	- <https://youtu.be/6-0zD9Xyu5c?si=VFMHtA06wN21DsHn&t=583>
- We can bake lights / occlusion culling for the entire level all at once, and the new lights / occlusion culling will show up in the individual scenes!
	- No more baking lights in someone's prefab level AND the apartment level!

## How Do We Do This?
- Each person is going to have their own scene(s)
- If you want to see what your scene looks like within the full level, just drag the other scenes into your scene real quick.
	- MAKE SURE NOT TO MAKE ANY CHANGES TO ANYONE ELSES SCENE WHILE YOU ARE DOING THIS. Me personally, I collapse the other scenes in the hierarchy just so I don't accidentally do something stupid in one of the other scenes.
- *NOTE*: when dragging in the other scenes, your scene *SHOULD* line up with the other scenes perfectly.

### What about Baking Lights & Occlusion Culling?
- ***To bake lighting / occlusion culling***, literally just drag in all the sub-scenes you want the lights / occlusion culling to apply to.
- Then bake normally.
- That's it. It *should* just work

### Some Thing to Keep in Mind
- The sub-scenes for the level *should* only contain the level itself.
- Do not put the player in your sub-scene.

### How Do I Get the Player in My Level so I Can Test it out Real Quick?
-
