# Overview

Audio in Relapse is handled by the `SoundManager` script, which can be found in the Global Object (which can be found on the player).

# Sound Manager

## Inspector

The `SoundManager` on the global object does not need to be edited in the Unity inspector; it should come with the correct setting already.

In the event it stops working:

- Make sure the 'Music Source' variable is set in the inspector to the `Music Source` object found in the global object.
- Make sure the 'SFX Source' variable is set in the inspector to the `SFX Source` object found in the global object.

## Script

The `SoundManager` script is responsible for playing all audio in the game. It has a number of functions that can be called to play different sounds.

```csharp
public void PlaySfxAtPoint(Sound sound, Vector3 pos);
```

This function plays a sound at a specific point in the world (given the correct settings are on the sound.)

The 'sound' variable is a reference to a `Sound` object, which is an object that holds a sound and some audio settings.

The 'pos' variable is the position in the world where the sound should be played.

The sound will be played as a one-shot, meaning that it will not loop and will not be stopped by another sound playing.

> NOTE: Even if a sound is set to loop, it will not loop when played with this function.

```csharp
public void PlayMusic(Sound sound);
```

This function plays a sound as music.

Sounds played with this function WILL get stopped by other sounds playing.

## Custom Classes

### Sound

A class that holds:

- an audio clip
- some sound settings.

### Sound Settings

A class that holds audio settings for a sound. This class is a scriptable object, which allows it to be edited in the Unity inspector.

This ***SCRIPT*** does not need to be interacted with. However, you may need to create a new SoundSettings scriptable object in the Unity inspector.

To do this, right-click in the Assets folder (preferably in Scriptable Objects > Sound Settings), go to Create > Audio > Sound Settings.

#### Notable Settings
- Loop: Whether the sound should loop or not. This should ONLY be used for music.
- Spatial Blend: How much the sound should be affected by 3D audio. 0 is 2D audio, 1 is 3D audio.
	- The default value of .95 is recommended for sound effects.
	- 0 is recommended for music.

### SoundPool

A class that holds an array of `Sound` so they can be played randomly. This can be used to play random sounds for things like footsteps or gunshots, which can add variety to the game.

## How to Use the Sound Manager to Play Your Own Sounds

Make a script with a serialized variable for a `Sound` object or `SoundPool` object. Assign the sound you want to play to this variable in the Unity inspector.

In the code itself, whenever you want to code, you can do the following:

```csharp
SoundManager.Instance.PlaySfxAtPoint(...);
```

```csharp
SoundManager.Instance.PlayMusic(...);
```
