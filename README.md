hi, thanks for picking up the mod!
this mod includes the restored & improved rhythm game editor in DELTARUNE Chapter 4 and the custom Black Knife chart.

***NOTE: This mod is currently built upon the RELEASE version of DELTARUNE.***
***You can downgrade to this version by running `download_depot 1671210 1671212 6530852604090871226` (to my knowledge) from your Steam console.***
***You can then access that version from `C:\Program Files (x86)\Steam\steamapps\content\app_1671210\depot_1671212`.***

# How to install:
- directly download this repository as a ZIP from the code folder (releasing it frequently would be too much of a hassle)
- using the Delta Patcher (DeltaPatcher.exe), patch your Chapter 4 data.win file using the rhythm_editor.xdelta file.
	- it is reccommended to BACKUP your original data.win file.
	- by selecting the backup original file option, the patch will be saved to dataPATCHED.win instead.
  - rename the new file to data.win.
- drag every *.txt file into your save directory
- create a save file with the dark world flag enabled that loads into either of the following:
	- room_rhythmgame_editor (access to the full chart editor and auto mode)
	- room_dw_rhythm_countdown (access to the track select and hard mode)
- it is NOT reccommended to load into any of the following:
	- room_dw_rhythm (unaccounted for; will very very very likely crash)
	- room_dw_castle_tv_rhythm (barely works, sends you to the track select anyway)
- open DELTARUNE and load said save file

# Features
- custom songs can be created, modified and deleted via the chart editor
- custom music files/pointers can be loaded through DELTARUNE's "mus" folder
- implementation of custom bpm and time signatures, including change mapping
- vanilla song list can be restored by deleting songlist.txt
- the chart editor provides quick access to auto, normal and hard mode
- some unused/debug keybinds were restored
## A note about stems
when creating a custom song, you will be asked to provide a "no guitar" stem and a "guitar" stem. these can either:
- be the same file (this will make them mutually exclusive in playthroughs)
- be one file with everything but the guitar stem, then one file with everything. (this is how stems are intended to work in DELTARUNE)
	- to signal the game of the "no guitar" stem, your filename must include "no_guit" anywhere in it.

glhf, and happy charting!

PS. original snippets of the vanilla rhythm minigame
(scores & ranks and the minigame room in castle town)
have been heavily modified (sometimes disabled) for the sake of customizability
