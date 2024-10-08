# Overview

![Explosion Power Example](<../../_META/Attachments/Pasted image 20241008131156.png>)

Powers in Relapse use Unity's [Scriptable Objects](https://docs.unity3d.com/Manual/class-ScriptableObject.html) as the basis of their implementation. This allows for easy modification of existing powers and the creation of new powers.

#### Anatomy of A Power

| Data Field                       | Description                                                                              |
| -------------------------------- | ---------------------------------------------------------------------------------------- |
| **Power name**                   | The name of the power that gets displayed in-game                                        |
| Power Type                       | Whether the power is drug-based or med-based                                             |
| Icon                             | The UI image for the power that is displayed in-game                                     |
| Description                      | A text box that will be shown to the user so they know what the power does.              |
| Charge Duration                  | How long the player has to hold the power button before being able to release the power. |
| Active Effect Duration           | **ONLY APPLIES TO SOME POWERS**. If the power has an active effect that lasts            |
| Cooldown Duration                |                                                                                          |
| Base Tolerance Meter Impact      |                                                                                          |
| Tolerance Meter Level Multiplier |                                                                                          |
| Power Logic Prefab               |                                                                                          |

# Modifying Existing Powers (Designer-Focused)

# Creating New Powers / Power Behavior (Code-Focused)
