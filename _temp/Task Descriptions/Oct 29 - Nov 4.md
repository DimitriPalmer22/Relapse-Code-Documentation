
## C# Research: Inhertiance, Interfaces, Abstraction

***GOAL***: The purpose of this is to get you even more familiar with using inheritance in C# since most scripts in the project use inheritance.

Videos:

- <https://www.youtube.com/watch?v=MZOrGXk4XFI&ab_channel=CodeMonkey>
- <https://www.youtube.com/watch?v=9atF8x1U6QI&ab_channel=GiraffeAcademy>
- <https://www.youtube.com/watch?v=qgU2ojOKLP8&ab_channel=tutorialsEU-C%23>

> Goal of Research: If a parent class or interface is not making sense, try to look at the classes that extend from it to see how it is properly implemented.

## C# Inheritance Personal Project

***GOAL***: The purpose of this is to build more confidence when working with inheritance / composition on your own.

> NOTE: This will be done in PURE C#. DO NOT MAKE A UNITY PROJECT FOR THIS. Make a project in Visual Studio instead.

### Project Prompt: "Animal Care System"

1. **Inheritance**:

	- Create an abstract class `Animal` with properties like `Name` (string) and `Age` (int), and an abstract method `MakeSound()` that returns a `string` (this string is unique to each type of animal)
	- Create two subclasses `Dog` and `Cat` that inherit from `Animal`. Each should implement `MakeSound()`, returning a unique sound (e.g., "Woof" for `Dog` and "Meow" for `Cat`).
2. **Composition**:

	- Define an interface `ICare` with methods `Feed()` (returns `string`) and `Play()` (returns `bool`).
	- Implement `ICare` in two classes, `DogCare` and `CatCare`. `Feed()` should return a message like "Dog has been fed" or "Cat has been fed," and `Play()` should return `true` if the animal is happy to play (could be based on random logic or age).
3. **Objective**:

	- Develop a console app where users can create animals, feed, and play with them. This should reinforce knowledge of inheritance and composition with clear return types.
	- The description for this personal project is intentionally a little loose because you are meant to play with it. Try to explore and discover things so you get more comfortable.

## C# Research: Events

***GOAL***: Get much more comfortable using events in C#. These are the basis for the collaborative system I have set up so that you can interact with my scripts and their logic without having to edit the scripts themselves.

Videos:

- <https://www.youtube.com/watch?v=3ZfwqWl-YI0&ab_channel=CodeMonkey>
- <https://www.youtube.com/watch?v=OuZrhykVytg&ab_channel=CodeMonkey>

## C# Events Personal Project

***GOAL***: Learn more about using events in C# so you can build more confidence when working on your own.

> NOTE: This will be done in PURE C#. DO NOT MAKE A UNITY PROJECT FOR THIS. Make a project in Visual Studio instead.

### Project Prompt: "Gaming Console System"

1. **Delegate and Events**:

	- Create a delegate `GameAction` with a `void` return type and a `string` parameter (`actionDescription`). This delegate will represent actions performed on a gaming console and will use the `actionDescription` parameter to detail each action.

	- In a `GameConsole` class, define three public events that use the `GameAction` delegate:

		- `OnGameStart` – triggered when a game starts.
		- `OnGamePause` – triggered when a game is paused.
		- `OnGameOver` – triggered when the game ends.
2. **Event Functions**:

	- For each event, create two methods to respond:
		- **Game Start**:
			- `DisplayWelcomeMessage(string actionDescription)` – prints "Welcome: \[actionDescription]".
			- `PlayIntroSound(string actionDescription)` – prints "Playing intro sound: \[actionDescription]".
		- **Game Pause**:
			- `ShowPauseMenu(string actionDescription)` – prints "Pause Menu shown: \[actionDescription]".
			- `MuteSound(string actionDescription)` – prints "Sound muted: \[actionDescription]".
		- **Game Over**:
			- `ShowGameOverScreen(string actionDescription)` – prints "Game Over Screen displayed: \[actionDescription]".
			- `PlayGameOverSound(string actionDescription)` – prints "Game Over sound played: \[actionDescription]".
3. **Main Function and Loop**:

	- In the `Main` method, create a loop to capture user input:
		- Entering `"start"` triggers the `OnGameStart` event.
		- Entering `"pause"` triggers the `OnGamePause` event.
		- Entering `"end"` triggers the `OnGameOver` event.
		- Entering `"quit"` breaks the loop and exits the program.
4. **Objective**:

	- The program provides an interactive simulation of a gaming console system, giving users practice with creating custom delegates, managing events, and responding dynamically based on user input.

## Simple Functioning Main Menu

A simple start menu for the sake of the vertical slice would make our game seem more polished.

The main menu should look like:

![](<../../_META/Excalidraw/exc_2024-10-29 20.50.48.excalidraw.png>)

***Start***: opens the ApartmentBlockout scene.

***Options***: Shows what WOULD be an options screen, but for now, that can be left empty.

***Credits***: Show everyone's name on the screen. Please divide us based on role. Look in the discord if you are confused on people's roles.
- Blue - Coder
- Green - designer
- Purple - artist

***Exit***: Quit the game (Normally, the Unity function to quit the game only works with an actual build of the game)

## New Power (Medicine) - Time Slow

### Quick Refresher on the Power System

Remember, powers in Relapse are composed of 3 parts:

- The power scriptable object that holds the general information for the power (name, cost, charge time, etc.)
	- Found in `Assets/Scriptable Objects/Powers`
	- To create a new power, right-click in this folder and select "Create > Power"
- The The power logic script that defines what the power does.
	- Found in `Assets/_Scripts/Player/Powers`
	- Make sure that this script extends from the `MonoBehaviour` class and implements the `IPower` interface.
- The power logic prefab that holds the logic script
	- Found in `Assets/Prefabs/Player/Power Logic`
	- Remember, this script needs to be put on an empty prefab and then dragged into the "Power Logic Prefab slot" in the power's scriptable object.

For more information, check the [Powers](<../../Documentation/Powers/Powers.md>) documentation.

> NOTE: to test your power, drag the scriptable object into the Powers list in the *PlayerPowerManager* component on the player.

### Time Slow Power Specifications

When activated, the Time Slow power will slow down the game's time scale for a short period. This will give the player more time to react to enemies and obstacles.

In the logic script,

- Use the `StartPassiveEffect(…)` function to slow down the time scale.
- Use the `EndPassiveEffect(…)` function to return the time scale to normal.
- The time scale that gets set when the power is applied should be a serialized field so that we can edit it in the inspector.

To adjust the duration of the slow down effect, you can use the `Passive Effect Duration` field in the power's scriptable object.

If you can, don't make the power immediately set the time scale back and forth. Try to smoothly transition between the time scales.

## Document the New Power

Write a word document or something describing how the power works. I'll make it look better and throw it in the wiki later.

Try to be as specific as possible with your documentation. It might also be a good idea to include function and variable names. This is so we can eventually use this for the TDD later on.

## Create Shotgun Logic

### Creating New Gun Information for the Shotgun

The weapon system uses scriptable objects to store the more general information about guns like name, damage, fire rate, etc.

This is done so that we can easily create new weapons without having to edit the scripts themselves.

1. Create a new scriptable object in `Assets/Scriptable Objects/Gun` called `Shotgun 1`.
2. Fill in the information for the shotgun. You can look at the pistol scriptable object for reference (or even copy over almost every field)
3. Make sure the shotgun is semi-automatic
4. The shotgun will use the 'Bloom Angle' variable to control its spread, so crank that value up a little.

### Create a New Script for The Shotgun

This script should go in `_Scripts/Gun` and should be called something along the lines of 'Shotgun'.

The script should extend from `Monobehavior` and implement the `IGun` interface.

```cs
public class Shotgun : MonoBehaviour, IGun
{
    // Your code here
}
```

Honestly, you can probably start off by copying the GenericGun script and removing things. It will save you a lot of time.

***THE BULK OF WHAT YOU NEED TO EDIT IS IN THE `FIRE()` FUNCTION***

#### Firing Multiple Pellets at once

The shotgun should shoot multiple bullets at once. The number of bullets should be editable in the inspector. We can represent this with a variable called `pelletsPerShot`.

To fire multiple pellets per shot, we can edit the line in the `Fire()` function that looks like:

```cs
for (var i = 0; i < timesToFire; i++)
```

We can change this to a line that looks like:

```cs
for (var i = 0; i < timesToFire * pelletsPerShot; i++)
```

This way, we can fire multiple bullets per shot. However, this creates a new problem. This will subtract `pellersPerShot` bullets from the player's `_currentMagazineSize`. This is not the intended behavior. We want the player to only lose one bullet from their magazine per shot.

To fix this, add the end of the function after the for loop, we can add `(pelletsPerShot - 1) * timesToFire` back to the player's magazine.

### Creating the Shotgun Prefab
- For this, you should be able to copy the pistol prefab and replace the model + weapon script.
	- Use the shotgun model located in `Prefabs/Player/Guns/Shotgun_no_anim`
	- Replace the generic gun script with the new shotgun script you just made.
	- Make sure the collider is set up properly on the shotgun model.
	- Make sure the shotgun script has the correct scriptable object applied to it.
### Making Sure it Works

The shotgun should be able to be "picked up" if the player looks at it and presses the interact button.

The shotgun should not be automatic. Make sure the player has to press and release the shoot button each time to shoot the weapon.

## Document the Shotgun Logic

Write a word document or something describing how the shotgun works. I'll make it look better and throw it in the wiki later.

Try to be as specific as possible with your documentation. It might also be a good idea to include function and variable names. This is so we can eventually use this for the TDD later on.
