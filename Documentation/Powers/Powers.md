# Overview

> This page does ***NOT*** contain information about how the back-end of the powers works. This page is meant to be a guide for designers / coders to understand how the powers work and how to modify them.

![Explosion Power Example](<../../_META/Attachments/Pasted image 20241008131156.png>)

### So What *Exactly* Do the Powers Do?

When the player holds the power button, they charge the currently equipped power. Once the power is fully charged and the player *releases* the power button, the power is activated. When the power is activated, the power's *immediate effect* is activated, the power's *active effect* is started, and the power's *passive effect* is started.

| Part of the Power | Description                                                                                                                                                                                                                                                                                                                                                                                                              |
| ----------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Charging Period   | A part of the power where the power has not been activated yet. Custom logic can be put here.                                                                                                                                                                                                                                                                                                                            |
| Immediate Effect  | A part of the power that activates as soon as the player activates the power.<br><br>The immediate effect does not have any continuous implications.<br><br>This is where projectiles are fired or explosions are activated.                                                                                                                                                                                             |
| Active Effect     | A ***CONTINUOUS*** part of the power that activates once the player activates the power.<br><br>The active effect is continuously applied while it is active.<br><br>For example, let's say our power is a flamethrower that stays on for 10 seconds.<br>The effect for continuously shooting fire would be part of the active effect.<br><br>***NOTE***: The player cannot switch powers while the active effect is on. |
| Passive Effect    | A ***CONTINUOUS*** part of the power that activates once the player activates the power.<br><br>This is where any background effects are continuously applied.<br><br>This is mostly used for status effects.<br><br>***NOTE***: If the power is re-activated while the current passive effect is active, the effects DO NOT stack.                                                                                      |
| Cooldown          | The part of the power where the player is not allowed to activate / charge the power.<br><br>Once the active effect is done, the cooldown is activated.<br><br>***NOTE***: If the power has no active effect duration, then the cooldown is activated immediately.                                                                                                                                                       |

![](<../../_META/Excalidraw/exc_2024-10-08 13.38.30.excalidraw.png>)

### Generally, How Are the Powers Implemented?

Powers in Relapse use a ***2-part system*** as the basis of their implementation:

- Unity's [***Scriptable Objects***](https://docs.unity3d.com/Manual/class-ScriptableObject.html), which allow for easy modification of existing powers and the creation of new powers. This is so designers can easily make their own changes to the simple behavior of the powers.
- Unity's [***Prefab System***](https://docs.unity3d.com/Manual/Prefabs.html), which allows for easy and modular implementation of power behavior. Each power has a prefab that contains a script with the logic for the power's behavior. For design purposes, each prefab ***SHOULD*** have variables that designers can easily modify without having to change the scripts themselves.

# Modifying Existing Powers (Designer-Focused)

### Anatomy of The Power Scriptable Object

| Data Field                       | Description                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| -------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Power name**                   | The name of the power that gets displayed in-game                                                                                                                                                                                                                                                                                                                                                                                                  |
| Power Type                       | Whether the power is drug-based or med-based                                                                                                                                                                                                                                                                                                                                                                                                       |
| Icon                             | The UI image for the power that is displayed in-game                                                                                                                                                                                                                                                                                                                                                                                               |
| Description                      | A text box that will be shown to the user so they know what the power does                                                                                                                                                                                                                                                                                                                                                                         |
| Charge Duration                  | How long the player has to hold the power button before being able to release the power                                                                                                                                                                                                                                                                                                                                                            |
| Active Effect Duration           | **ONLY APPLIES TO SOME POWERS**. If the power has an active effect that lasts, this field represents how long that power is active                                                                                                                                                                                                                                                                                                                 |
| Cooldown Duration                | How long before the player is able to use the power again after using it                                                                                                                                                                                                                                                                                                                                                                           |
| Base Tolerance Meter Impact      | How much the tolerance meter goes up or down after using the power. Drugs add this value to the tolerance meter, while meds subtract                                                                                                                                                                                                                                                                                                               |
| Tolerance Meter Level Multiplier | Based on what level the power is (in terms of upgrades), a multiplier is applied to the tolerance meter impact when using the power.<br><br>When the player uses the power, the total tolerance meter impact is calculated like:<br>Total Impact = (Base Impact) * (Current Level Multiplier)<br><br>So, drug-based powers should have multipliers <= 1 when upgrading them.<br>Med-based powers should have multipliers >= 1 when upgrading them. |
| Power Logic Prefab               | A prefab that contains the actual logic for how the power works. A power without this won't do anything.                                                                                                                                                                                                                                                                                                                                           |

# Creating New Powers / Power Behavior (Code-Focused)

All prefabs that contain the power logic ***NEED*** a script on them that implements the [IPower interface](https://github.com/aidenr2023/Relapse/blob/main/Assets/_Scripts/Powers/IPower.cs)! You ***NEED*** to understand interfaces in C# to implement this correctly!

```cs 
public class Fireball : MonoBehaviour, IPower {}
```

> ***NOTE***: You can also look at the comments in the IPower interface for more clarification on what each method does.

More Resources on Interfaces and Inheritance in C#:

- <https://www.programiz.com/csharp-programming/inheritance>
- <https://www.codecademy.com/resources/docs/c-sharp/interfaces>

### Creating the Prefab

When creating a new prefab to store the power logic, make the prefab based on an empty game object. We want the prefab to be invisible.

> Nerd stuff: Why does the prefab need to be an empty game object?
> You see, the each power logic prefab is actually instantiated whenever the player uses the corresponding power. However, I made it so that the instantiated game objects are invisible in the hierarchy so that the player / designer doesn't accidentally mess with them. The entire system was designed this way so that the power manager can access the power logic in a static manner.

Once the empty game object is made, you need to add a script to it that implements the IPower interface. This script will contain the logic for the power.

That's it. You're done!

### Adding the Power Logic Prefab to the Scriptable Object

Once you've finished creating your prefab, you need to add it to the Scriptable Object. This is done by dragging the prefab into the `Power Logic Prefab` field in the Scriptable Object.

### Important Functions Of the Interface

> ***NOTE***: You can look at the `Assets/_Scripts/Powers/Drugs/Fireball.cs` or `Assets/_Scripts/Powers/Drugs/Explosion.cs` scripts to see examples of how to use the interface's functions!

```cs
public void Charge(TestPlayerPowerManager powerManager, PowerToken pToken);
```

Charge() - This function is continuously called while the player is charging the power. This is where you can put custom logic for the power's charging period.

---

```cs
public void Use(TestPlayerPowerManager powerManager, PowerToken pToken);
```

Use() - This function is called when the player releases the power button. This is where you can put custom logic for the power's immediate effect.

---

```cs
public void UpdateActiveEffect(TestPlayerPowerManager powerManager, PowerToken pToken);
```

UpdateActiveEffect() - This function is called every frame while the power is active. This is where you can put custom logic for the power's active effect.

There are also some other functions that can be used to assist with active effect logic:

```cs
public void StartActiveEffect(TestPlayerPowerManager powerManager, PowerToken pToken);

public void EndActiveEffect(TestPlayerPowerManager powerManager, PowerToken pToken);
```

---

```cs
public void UpdatePassiveEffect(TestPlayerPowerManager powerManager, PowerToken pToken);
```

UpdatePassiveEffect() - This function is called every frame while the power is active. This is where you can put custom logic for the power's passive effect.

There are also some other functions that can be used to assist with passive effect logic:

```cs
public void StartPassiveEffect(TestPlayerPowerManager powerManager, PowerToken pToken);

public void EndPassiveEffect(TestPlayerPowerManager powerManager, PowerToken pToken);
```

### Alright, Now How *EXACTLY* Do I Implement This Correctly?

First and foremost, NEVER, and I MEAN NEVER, manually instantiate the power logic anywhere or at any time. You do not need to do this. You should not need to do this. If you ever do this, you are using the system incorrectly!

The power logic scripts are supposed to be used as if they are static objects. Treat the functions inside this script as if they are static functions. Avoid using `this` or `gameObject` in the script. The functions are set up with parameters that make it easy to access the player's power manager and the power token.

#### What is a Power Token?

The power tokens are used to store the individual data for each power. For example, they store how much remaining cooldown or active time the power has. The current power's corresponding power token is passed into the power logic functions so that the power logic can access the data stored in the token.

#### You Can Use the Power Token To Store Even More Data

Inside the `PowerToken` class is a `Dictionary<string, object>` that you can use to store any extra data you need for the power. This is useful for storing data that you need to access in multiple functions.

To store data in this dictionary, use the `AddData(…)` function within the `PowerToken` class. Using this function you can store ANY type of data you want with an associated key. It is a good idea to make this key a constant value that can only be accessed within that specific power logic script.

To retrieve data, use the `RemoveData(…)` function within the `PowerToken` class. This function will return the data stored at the key you provide.

The `Assets/_Scripts/Powers/Meds/DamageIncrease.cs` script is a 