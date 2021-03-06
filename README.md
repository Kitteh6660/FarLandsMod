## Far Lands Mod [![downloads](https://img.shields.io/github/downloads/ThisTestUser/FarLandsMod/total.svg)](https://github.com/ThisTestUser/FarLandsMod/releases/latest)
A mod to restore the far lands in Forge. This mod was made for 1.12.2, but should theoretically work from 1.8 to 1.12.2.

Here is the far lands mod for 1.13 and above: https://github.com/ThisTestUser/FarLandsModV2

## Links
To download the mod, head to the releases page.

The first time you load the mod, you will see a config file generate at %mc_dir%/configs/farlandsmod.cfg.

You can use the config file to edit certain features of this mod.

To view an exploration of the far lands, check out the link below. (Note: You will need to edit some of the dimension mods to make it compatible with the far lands)

https://github.com/ThisTestUser/FarLandsChronicles

### How does this work?
This mod works by using ASM to directly patch NoiseGeneratorOctaves.class.
From beta 1.8 to 1.13.2, the following code below is used to fix the far lands:
```
k = k % 16777216L;
l = l % 16777216L;
```
By removing these modulos, we can allow the integers to overflow and add back the far lands!

### What makes this mod different?
While there are other Far Lands mods out there, this mod uses the quickest way to add back the far lands. The fact that we don't override anything and only change 2 lines means that we could potentially create the Far Lands in **other dimensions** as well!

For example, here is the far lands in Twilight Forest.
![twilightforest](https://user-images.githubusercontent.com/15678918/46991807-6d96a200-d0d5-11e8-9c81-5a811e48b7a5.png)
And here it is in planet Neptune (Galaticcraft extra planets mod)
![neptune](https://user-images.githubusercontent.com/15678918/47047805-ad599a00-d166-11e8-9198-05b096f6f4a9.png)
Note that dimensions that do not use the vanilla terrain generator will not have the far lands enabled.
