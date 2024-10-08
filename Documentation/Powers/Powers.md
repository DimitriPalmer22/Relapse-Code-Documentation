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
- Unity's [***Prefab System***](https://docs.unity3d.com/Manual/Prefabs.html), which allows for easy and modular implementation of power behavior. Each power has a prefab that contains a script with the logic for the power's behavior.

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
#### Important Functions Of the Interface

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
