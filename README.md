# Difficulty Slider MCM

# Changelog
1.0 
* Initial Release

1.1 
* Updated description of setting to fit ObRe. Changed how the command is processed in the Ini file. no longer relies on an ObScript watcher
* No longer requires an ESP, just the ini file. 

## Description

* Note: This will still affect damage done and received in the ObRe 1.2 patch as this mod does not, and will never, change actual difficulty settings, and only changes the damage multiplier the game uses to calculate damage done.

* Mod Configuration Menu (MCM) for controlling the Difficulty Damage Multiplier
* Supports values between -20 and 20

1. fDifficultyDamageMultiplier
* Default: 5.00
* Description=Default: 5.0 Min: -20 Max: 20 Increment: 0.1. | Difficulty affects how much damage the player does in combat, and how much damage they receive. Damage of all types is affected by Difficulty. This multiplier is the maximum amount the damage the player can do when difficulty is set to Novice. It divides the amount of damage done to the player by the same value. Difficulty Settings can be made more subtle by lowering this value, and more extreme by raising it.

(Player will receive 1/5th normal damage and deal 5x normal damage on Novice).
(Player will receive 1/3.5th normal damage and deal 3.5x normal damage on Apprentice).
(Player will receive 1x normal damage and deal 1x normal damage on Adept). 
(Player will receive 3.5x normal damage and deal 1/3.5th normal damage on Apprentice).
(Player will receive 5x normal damage and deal 1/5th normal damage on Master).

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