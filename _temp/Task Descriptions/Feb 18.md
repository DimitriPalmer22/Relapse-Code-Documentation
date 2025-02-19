# Weapon Balancing

In Relapse, the player will (eventually) have the ability to purchase newer, more powerful versions of the guns in the vendor areas. We need the weapons that the player can buy to be more balanced.

Every weapon has a base version (the name of it ends with 1) that is the weakest version of the weapon. The other versions of the weapon are stronger and more expensive (the number at the end of the weapon's name increases with the weapon's power).

### How to Change the Gun Values

The guns are composed of two main parts:

- The scriptable object that contains the gun's stats
- The gun prefab

You will be editing the guns' scriptable objects to balance the weapons. The scriptable objects for the guns are located in `/Assets/Scriptable Objects/Gun_SO`.

DO NOT REBALANCE THESE GUNS. THEY WILL NOT BE USED!:

- Shotgun 1
- Shotgun 2
- Shotgun 3
- Hand Cannon

### Balancing Tips

Think of each weapon's weakest component. The stronger versions of that weapon *could* improve that component. For example, the pistol has a low rate of fire.
#### Pistol

The pistol is supposed to be the most reliable weapon in the game. Do not think of the pistol as the weakest weapon in the game. It should be strong enough that it is a viable option for the player to use.

The pistol focuses on accuracy, long range, and decent damage over a long distance. The pistol's limiting factor is it's semi-automatic firing mode and its lower rate of fire. Player's who are able to hit their shots consistently will be rewarded when using this weapon.

#### Automatic Pistol

The automatic pistol is the game's fully automatic weapon. It is supposed to be the hardest weapon to control, but it should also have the highest rate of fire.

The automatic pistol focuses on rate of fire, medium range, and decent damage. The automatic pistol's limiting factors are its recoil and magazine capacity. Players who are able to control the automatic pistol's recoil and properly manage their ammo will be rewarded when using this weapon.

#### Shotgun

# Power Balancing
-
