# Overview

![Explosion Power Example](<../../_META/Attachments/Pasted image 20241008131156.png>)

#### So What Do the Powers Do?

uhhh

![](<../../_META/Attachments/Pasted image 20241008134516.png>)

#### Generally, How Are the Powers Implemented?

Powers in Relapse use a ***2-part system*** as the basis of their implementation:

- Unity's [***Scriptable Objects***](https://docs.unity3d.com/Manual/class-ScriptableObject.html), which allow for easy modification of existing powers and the creation of new powers
- Unity's [***Prefab System***](https://docs.unity3d.com/Manual/Prefabs.html), which allows for easy and modular implementation of power behavior

# Modifying Existing Powers (Designer-Focused)

#### Anatomy of The Power Scriptable Object

| Data Field                       | Description                                                                                                                          |
| -------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------ |
| **Power name**                   | The name of the power that gets displayed in-game                                                                                    |
| Power Type                       | Whether the power is drug-based or med-based                                                                                         |
| Icon                             | The UI image for the power that is displayed in-game                                                                                 |
| Description                      | A text box that will be shown to the user so they know what the power does                                                           |
| Charge Duration                  | How long the player has to hold the power button before being able to release the power                                              |
| Active Effect Duration           | **ONLY APPLIES TO SOME POWERS**. If the power has an active effect that lasts, this field represents how long that power is active   |
| Cooldown Duration                | How long before the player is able to use the power again after using it                                                             |
| Base Tolerance Meter Impact      | How much the tolerance meter goes up or down after using the power. Drugs add this value to the tolerance meter, while meds subtract |
| Tolerance Meter Level Multiplier | If the player upgrades the power,                                                                                                    |
| Power Logic Prefab               |                                                                                                                                      |

# Creating New Powers / Power Behavior (Code-Focused)

…
