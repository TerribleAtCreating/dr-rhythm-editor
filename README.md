hi, thanks for picking up the mod!
this mod includes the restored & improved rhythm game editor in DELTARUNE Chapter 4 and the custom Black Knife chart.

# Versioning DELTARUNE for the mod
This mod is built upon the release version of DELTARUNE from Steam.
The version supported by this mod can be reached using these IDs:
- `App ID`: 1671210
- `Depot ID`: 1671212
- `Manifest ID`: 6530852604090871226

IF you have bought DELTARUNE on Steam, you can first open up Steam's console by pressing `Win + R` and running `steam://open/console`.
You can downgrade DELTARUNE by running `download_depot 1671210 1671212 6530852604090871226` from your Steam console.
You can then access that version from `C:\Program Files (x86)\Steam\steamapps\content\app_1671210\depot_1671212`. (adapt as needed)

# Mod setup
- Directly download this repository (from the `main` branch) as a ZIP from the code folder (releasing it frequently would be too much of a hassle)
- Using the Delta Patcher (DeltaPatcher.exe), patch your Chapter 4 data.win file using the rhythm_editor.xdelta file.
	- It is reccommended to BACKUP your original data.win file.
	- By selecting the backup original file option, the patch will be saved to `dataPATCHED.win` instead.
	- Rename this new file to data.win.
- Drag every *.txt file into your save directory
- For the following step, it is reccommended to have a lookup table or save editor for the room names.
- Create a save file with the dark world flag enabled that loads into either of the following:
	- `room_rhythmgame_editor` (access to the full chart editor and auto mode)
	- `room_dw_rhythm_countdown` (access to the track select and hard mode)
- It is NOT reccommended to load into any of the following:
	- `room_dw_rhythm` (unaccounted for; will very very very likely crash)
	- `room_dw_castle_tv_rhythm` (barely works, only points to the first 3 songs)
- Open DELTARUNE and load said save file

# Features
- Custom songs can be created, modified and deleted via the chart editor
- Custom music files/pointers can be loaded through DELTARUNE's "mus" folder
- Quick access to other tracks from the rhyhm game via the retry prompt
- Implementation of custom BPM and time signatures, including change mapping
- Vanilla song list can be restored by deleting songlist.txt
- Quick access to auto, normal and hard mode via the chart editor
- Restoration of some unused/debug keybinds
## A note about stems
When creating a custom song, you will be asked to provide a "no guitar" stem and a "guitar" stem. these can either:
- Be the same file (this will make them mutually exclusive in playthroughs)
- Be one file with everything but the guitar stem, then one file with everything. (this is how stems are intended to work in DELTARUNE)
	- To signal the game of the "no guitar" stem, your filename must include "no_guit" anywhere in it.

GLHF, and happy charting!

P.S. Original snippets of the vanilla rhythm minigame
(scores & ranks and the minigame room in castle town)
have been heavily modified (sometimes disabled) for the sake of customizability
