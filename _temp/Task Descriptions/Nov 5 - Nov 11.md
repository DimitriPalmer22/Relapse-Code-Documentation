#### Research: Events In Games

This is to get more information on how events are implemented in games. The goal is to understand how they are used and how they are implemented.

- <https://www.youtube.com/watch?v=A7jJq7O7u7A&ab_channel=Tutemic>

#### Research: Design Pattern - Singleton

The goal is to understand how the Singleton design pattern is used in game development. This is used all throughout Relapse, so it is important to understand how it works.

- <https://www.youtube.com/watch?v=VTZ1TQR80Qc&ab_channel=NickProud>

#### Research: Encapsulation

The goal is to understand how encapsulation is used in collaborative development. Good coding practices are important to understand when working on a team.

- <https://www.youtube.com/watch?v=8FmE_-QXg3Y&ab_channel=BroCode>
- <https://www.youtube.com/watch?v=EgfRA_PG25M&ab_channel=CalebCurry>

#### Personal Project: Singleton and Encapsulation

***Make this project inside of Unity.***

> Make sure to use the **New Input System** for this project. One of the later tasks requires it, so it's best to start using it now.

> You should probably use your knowledge of events as well to make this project more interesting.

Create a small project where you implement a `GameManager` class using the Singleton design pattern. This Game Manager will manage a simple game's score and game state. You'll also create three other classes:

- `Player`: health, player movement, shoot input, decrease score on hit
- `Enemy`: health, enemy movement, update score on death
- `UIManager`: managing a UI element that displays the score

Each of which will reference the Game Manager to retrieve or modify the score and check if the game is over.

Your Game Manager should use encapsulation to keep its current score field private, providing public properties / methods to get or set these values as needed.

- To be specific, the variable / field that holds the score should be private.
- There should a public getter PROPERTY to get the score.
- There should be a public setter FUNCTION to set the score to a specific value.

#### Research: Scriptable Objects
