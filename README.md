# [ObRe 1.2] Dynamic Difficulty Multiplier (MCM)

# Changelog
1.0
* Complete rebuild and re-release. 

## Description

* Mod Configuration Menu (MCM) for controlling the Difficulty Damage Multiplier for all 1.2 difficulties.

* As of version 1.2, ObRe now calcuates damage done based on 2 different sliders the player chooses. Dicene explored UE and found 12 new game settings that govern damage done and dealt. This mod is built to dynamically adjust all of those settings depending on the player set fDamageDifficultyMultiplier. 

* I cannot attest to how accurate this math is to the actual math the game uses in calculations, but this should give you an idea of damage taken / received at different difficulties, and how you will conceivably  modify it by changing fDamageDifficultyMultiplier in the MCM.


1. fDifficultyDamageTakenMultiplierMaster = 5.0
	Master Damage Taken
	n = Damage
	Fn = (DDM+1)*n
	Fn = (5.0+1)*n
	Fn = 6.0n
	Master Damage Taken = 6x Normal Damage

1. fDifficultyDamageDealtMultiplierMaster = 5.0
	Master Damage Dealt
	n = Damage
	Fn = (1/(DDM+1))n
	Fn = (1/(5+1))n
	Fn = (1/6)n
	Fn = 0.167n
	Master Damage Dealt = 0.167x Normal Damage

2. fDifficultyDamageTakenMultiplierExpert = 2.5
	Expert Damage Taken
	n = Damage
	Fn = (DDM+1)*n
	Fn = (2.5+1)*n
	Fn = 3.5n
	Expert Damage Taken = 3.5x Normal Damage

2. fDifficultyDamageDealtMultiplierExpert = 2.5
	Expert Damage Dealt
	n = Damage
	Fn = (1/(DDM+1))n
	Fn = (1/(2.5+1))n
	Fn = (1/3.5)n
	Fn = 0.286n
	Expert Damage Dealt = 0.286x Normal Damage

3. fDifficultyDamageTakenMultiplierJourneyman = 1.5
	Journeyman Damage Taken
	n = Damage
	Fn = (DDM+1)*n
	Fn = (1.5+1)*n
	Fn = 2.5n
	Journeyman Damage Taken = 2.5x Normal Damage

3. fDifficultyDamageDealtMultiplierJourneyman = 1.5
	Journeyman Damage Dealt
	n = Damage
	Fn = (1/(DDM+1))n
	Fn = (1/(1.5+1))n
	Fn = (1/2.5)n
	Fn = 0.4n
	Journeyman Damage Dealt = 0.4x Normal Damage

4. fDifficultyDamageTakenMultiplierAdept = 0.0
	Adept Damage Taken
	n = Damage
	Fn = (DDM+1)*n
	Fn = (0+1)*n
	Fn = 1n
	Adept Damage Taken = 1x Normal Damage

4. fDifficultyDamageDealtMultiplierAdept = 0.0
	Adept Damage Dealt
	n = Damage
	Fn = (1/(DDM+1))n
	Fn = (1/(0+1))n
	Fn = (1/1)n
	Fn = 1n
	Adept Damage Dealt = 1x Normal Damage

5. fDifficultyDamageTakenMultiplierApprentice = -2.5
	Apprentice Damage Taken
	n = Damage
	Fn = (1/(DDM+1))n
	Fn = (1/(2.5+1))n
	Fn = (1/3.5)n
	Fn = 0.286n
	Apprentice Damage Taken = 0.286x Normal Damage

5. fDifficultyDamageDealtMultiplierApprentice = -2.5
	Apprentice Damage Dealt
	n = Damage
	Fn = (DDM+1)*n
	Fn = (2.5+1)*n
	Fn = 3.5n
	Apprentice Damage Dealt = 3.5x Normal Damage
	
6. fDifficultyDamageDealtMultiplierNovice = -5.0
	Novice Damage Taken
	n = Damage
	Fn = (1/(DDM+1))n
	Fn = (1/(5+1))n
	Fn = (1/6)n
	Fn = 0.167n
	Novice Damage Taken = 0.167x Normal Damage
	
6. fDifficultyDamageTakenMultiplierNovice = -5.0
	Novice Damage Dealt
	n = Damage
	Fn = (DDM+1)*n
	Fn = (5.0+1)*n
	Fn = 6.0n
	Novice Damage Dealt = 6x Normal Damage

### Prerequisites
1. [UE4SS](https://www.nexusmods.com/oblivionremastered/mods/32)
	1. [Mad OBScript Extender v2.0a or Later](https://www.nexusmods.com/oblivionremastered/mods/4819)
	2. [Mad Config Menu MCM v3.6 or later](https://www.nexusmods.com/oblivionremastered/mods/4810)
	
### Installation
0. Install Prerequisites
1. Copy Difficulty_Damage_Multipliers.esp to `\Oblivion Remastered\OblivionRemastered\Content\Dev\ObvData\Data`
	1. Add `Difficulty_Damage_Multipliers.esp` to your Plugins.txt
2. Copy Difficulty_Damage_Multipliers.ini to `\Oblivion Remastered\OblivionRemastered\Binaries\Win64\MadConfigs`

### Uninstallation
0. MCM Reset Method (Preferred)
	0. In the MCM, press 'Reset' to restore the Difficulty Settings to their default values before removing the Ini and ESP file
	
1. Batch file Method
	0. If you have already removed the ESP and INI file, and still need to restore default settings, do the following. 
	1. Download Restore_Difficulty.txt from GitHub [Link](https://github.com/justv316/Difficulty_Slider_MCM/blob/main/src/OblivionRemastered/Restore_Difficulty.txt)
	2. Copy the txt file to `\Oblivion Remastered\OblivionRemastered\Binaries`
	3. While In-game, press the ~ key to open the console, type `exec Restore_Difficulty` and press enter.
	4. The default settings have now been restored

2. Manual Method
	0. While In-game, press the ~ key to open the console. Type each command and press enter.
		`SetGameSetting fDifficultyDamageDealtMultiplierNovice -5`
		`SetGameSetting fDifficultyDamageTakenMultiplierNovice -5`
		`SetGameSetting fDifficultyDamageDealtMultiplierApprentice -2.5`
		`SetGameSetting fDifficultyDamageTakenMultiplierApprentice -2.5`
		`SetGameSetting fDifficultyDamageDealtMultiplierJourneyman 1.5`
		`SetGameSetting fDifficultyDamageTakenMultiplierJourneyman 1.5`
		`SetGameSetting fDifficultyDamageTakenMultiplierExpert 2.5`
		`SetGameSetting fDifficultyDamageDealtMultiplierExpert 2.5`
		`SetGameSetting fDifficultyDamageTakenMultiplierMaster 5`
		`SetGameSetting fDifficultyDamageDealtMultiplierMaster 5`

## Credits
1. Utilizes ObScript Extender created by [MadAborModding](https://next.nexusmods.com/profile/MadAborModding)
2. Utilizes MCM created by [MadAborModding](https://next.nexusmods.com/profile/MadAborModding)