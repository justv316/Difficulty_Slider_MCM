# Difficulty Slider MCM

# Changelog
1.0 
* Initial Release

## Description
![Difficulty Slider](/image/Difficulty_Slider.png "Difficulty Slider")

* Mod Configuration Menu (MCM) for controlling the Difficulty Damage Multiplier
* Supports values between 0.1 and 20
* You can check the console for the most recent values as they are printed there when the script runs. This also verifies if it's working. 

1. fDifficultyDamageMultiplier
	* Default: 5.00
	* Description: The difficulty slider affects how much damage the player does in combat, and how much damage they receive. Damage of all types, magical and mundane, is affected by the slider. This multiplier is the maximum amount the damage the player can do if the slider is set all the way to easy. 
	* It divides the amount of damage done to the player by the same value. If the slider is set all the way to hard, these values are inverted. This multiplier is reduced when the slider is set to in between values. The difficulty slider can be made more subtle by lowering this value, and more extreme by raising it.

### Prerequisites
1. [UE4SS](https://www.nexusmods.com/oblivionremastered/mods/32)
	1. [Mad OBScript Extender v2.0a or Later](https://www.nexusmods.com/oblivionremastered/mods/4819)
	2. [Mad Config Menu MCM](https://www.nexusmods.com/oblivionremastered/mods/4810)
	
### Installation
0. Install Prerequisites
1. Copy Difficulty_Slider_MCM.esp to `\Oblivion Remastered\OblivionRemastered\Content\Dev\ObvData\Data`
	1. Add `Difficulty_Slider_MCM.esp` to your Plugins.txt
2. Copy Difficulty_Slider_MCM.ini to `\Oblivion Remastered\OblivionRemastered\Binaries\Win64\MadConfigs`

### Uninstallation
0. This mod alters Game Settings. If you need to uninstall this, do the following after the plugin is removed.
	1. While In-game, press the ~ key to open the console, type `SetGameSetting fDifficultyDamageMultiplier 5` and press enter.
	
### Compatibility
0. Mods that manually set GameSettings seemingly will overwrite anything set by console command
1. This also seemingly applies to Settings set by [GameSettings Loader](https://www.nexusmods.com/oblivionremastered/mods/746) ini files.

## Credits
1. Utilizes ObScript Extender created by [MadAborModding](https://next.nexusmods.com/profile/MadAborModding)
2. Utilizes MCM created by [MadAborModding](https://next.nexusmods.com/profile/MadAborModding)