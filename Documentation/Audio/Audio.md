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

```
