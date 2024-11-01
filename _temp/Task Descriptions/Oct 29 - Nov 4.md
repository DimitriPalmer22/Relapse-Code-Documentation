
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
- The power logic prefab that holds the logic script
	- Found in `Assets/Prefabs/Player/Power Logic`
	- Remember, this script needs to be put on an empty prefab and then dragged into the "Power Logic Prefab slot" in the power's scriptable object.

For more information, check the [Powers](<../../Documentation/Powers/Powers.md>) documentation.

### Time Slow Power

When activated, the Time Slow power will slow down the game's time scale for a short period. This will give the player more time to react to enemies and obstacles.


## Document the New Power

## Create Shotgun Logic

## Document the Shotgun Logic
