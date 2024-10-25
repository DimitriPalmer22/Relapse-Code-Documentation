# Overview

Audio in Relapse is handled by the `SoundManager` script, which can be found in the Global Object (which can be found on the player).

### Sound Manager

#### Inspector

The `SoundManager` on the global object does not need to be edited in the Unity inspector; it should come with the correct setting already.

In the event it stops working:

- Make sure the 'Music Source' variable is set in the inspector to the `Music Source` object found in the global object.
- Make sure the 'SFX Source' variable is set in the inspector to the `SFX Source` object found in the global object.

#### Script

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

This function plays a sound as music. The sound will loop until it is stopped.
