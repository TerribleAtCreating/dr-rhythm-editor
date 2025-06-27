hi, thanks for picking up the mod!
this mod includes the restored & improved rhythm game editor in DELTARUNE Chapter 4 and the custom Black Knife chart.

# Downgrading DELTARUNE for the mod
This mod is built upon the release version of DELTARUNE from Steam.
The version supported by this mod can be reached using these IDs:
- `App ID`: 1671210
- `Depot ID`: 1671212
- `Manifest ID`: 6530852604090871226

IF you have bought DELTARUNE on Steam, you can first open up Steam's console by pressing `Win + R` and running `steam://open/console`.
You can downgrade DELTARUNE by running `download_depot 1671210 1671212 6530852604090871226` from your Steam console.
You can then access that version with the path provided by the console after finish.

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
- Custom Ralsei lyrics and censored/family-friendly lyrics
- Vanilla song list can be restored by deleting songlist.txt
- Quick access to auto, normal and hard mode via the chart editor
- Restoration of some unused/debug keybinds (and some brand-new ones)

# Discrepancies
## Character chart differences
When making charts for DELTARUNE, choosing a specific character instrument will result in the following changes:
### Susie \[Drums\]
- Only has the ability to play regular notes on two lanes.
### Kris \[Lead\]
- Has the full potential of the two-lane system, including regular notes, held notes and double notes.
### Ralsei \[Vocals\]
- Has access to an additional lane, totalling to three lanes.
- Defaults to placing held notes.
- When converting a held note back to a regular one, it is transformed into a tambourine note that matches the lane color (and vice versa).
- Cannot play multiple notes at once.
- Has the only note chart render to have an arrow under it in-game.
- His notes control the timing for the lyrics (if any).
## Reserved song IDs
The original DELTARUNE contains hardcoded cases for a few specific songs. These include:
- `"karaoke"` (Raise Up Your Bat)
- `"tutorial"` (Magically playing demo)
- `"practice"` (Sound Test)
- `"board4"` (The super awesome Doom Board rhythm game)
- `"knockyoudown"` (Knock You Down!!)

The songs listed above contain animation or temporal events that may interfere with your charts.
The charts themselves, however, are not affected by these.
## Configuring stems in songs
When creating a custom song, you will be asked to provide a "no guitar" stem and a "with guitar" stem. these can either:
- Be the same file (this will make them mutually exclusive in playthroughs)
- Be one file with everything but the guitar stem, then one file with everything respectively. (this is how stems are intended to work in DELTARUNE)
	- To signal the game of the "no guitar" stem, your filename must include "no_guit" anywhere in it.

# Lyrical syntax
- Words get seperated by spaces and get played on a vocal note (Ralsei's track)
- Ralsei's censored lyrics can be added by using `[width:lyric]`, where width is the equivalent amount of characters.
	- For example, FIGHT can be censored to `[5:ACT]` or `[5:PACIFY]`
- Hyphens (-) alter the syllable matching
	- For example, `SMILING` can be seperated by typing `SMIL-ING`
 	- This also means you can't include rendered hyphens in your lyrics
- Adding a lyric hiding cue basically involves leaving it empty
- You can also extend the censored lyrics past the actual lyrics if you so wish...

GLHF, and happy charting!

P.S. Original snippets of the vanilla rhythm minigame
(scores & ranks and the minigame room in castle town)
have been heavily modified (sometimes disabled) for the sake of customizability
