hi, thanks for picking up the mod!
this mod includes the restored & improved rhythm game editor in DELTARUNE Chapter 4 and the custom Black Knife chart.
made with [UndertaleModTool](https://github.com/UnderminersTeam/UndertaleModTool)

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
	
 	![image](https://github.com/user-attachments/assets/902f3c12-b6a6-4dee-b653-9783b8eb9ab9)
  	![image](https://github.com/user-attachments/assets/66bce0a0-314e-4b8a-a3c1-0aa5eca7d1d2)
	- By selecting the backup original file option, the patch will be saved to `dataPATCHED.win` instead.
	- Rename this new file to data.win.
- Drag every *.txt file into your save directory
- When opening Chapter 4, you will be greeted with a debug screen. You can go straight to Lightners Live or in this case, load into the chart editor.
- If you did all of the steps above, your editor will look like this:

![image](https://github.com/user-attachments/assets/373fe637-10fb-43e1-9469-1618980eed8e)

# Features
- Custom songs can be created, modified and deleted via the chart editor
- Custom music files/pointers can be loaded through DELTARUNE's "mus" folder
- Quick access to other tracks from the rhyhm game via the retry prompt
- Implementation of custom BPM and time signatures, including change mapping
- Custom Ralsei lyrics and censored/family-friendly lyrics
- Vanilla song list can be restored by deleting songlist.txt
- Quick access to auto, normal and hard mode via the chart editor
- Restoration of some unused/debug keybinds (and some brand-new ones)
## Additional keyboard shortcuts
(sourced from real shortcuts and not indicated in the tooltips)
- `(Hold) Delete`: Deletes all notes you highlight
- `Ctrl + C`: Copy all notes one measure ahead
- `Ctrl + V`: Paste all notes into the next measure(s)
	- `Ctrl + Shift + [C or V]`: Above command but with two measures
	- These do not affect your actual clipboard
- `Ctrl + X`: Cuts notes (copies notes, then deletes them)
- `Ctrl + S`: Replacement for vanilla's `U`, saves your chart
- `Ctrl + O`: Replacement for vanilla's `I`, loads a chart from a chosen source

# Discrepancies
## Stacked notes
There may be times where you are able to place two identical notes on top of eachother.
If that happens, your note will be highlighted red, as shown here:

![image](https://github.com/user-attachments/assets/d8b68f23-dc6d-4f27-b51b-b47fcb452f57)
## Character chart differences
When making charts for DELTARUNE, choosing a specific character instrument will result in the following changes:
### Susie \[Drums\]
- Only has the ability to play regular notes on two lanes.
- When attempting to extend a note, you will be moved to a ghost lane that would have the third note.
    - Placing a note in this state will create an orange line, as seen in "Raise Up Your Bat".
    - To delete these types of notes, hover over said ghost lane where the note would be, and right click as usual.
    - This ghost lane is very prone to note stacking due to how it was handled. Be cautious.
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
## Saving and loading songs
Whenever you save a song within the editor, it is automatically sent to your save file directory, this is also the case for vanilla songs.
A GameMaker limitation however saves the songs with the timestamps truncated to two decimal places. The chart will differ *very* slightly but probably won't cause any major issues.
- Song data files suffixed with `_autosave.txt` can be loaded using the autosave option with `Ctrl + O`.
- Song data files suffixed with `_export.txt` should be modded into the game manually, but this is completely optional.

To send custom charts to others, you must provide all 3-5 (depending on what you edited) song data files and the `songlist.txt` file.
These will automatically be processed by the mpd and will allow you and others to play the chart you made.
## Configuring stems in songs
When creating a custom song, you will be asked to provide a "no guitar" stem and a "with guitar" stem. these can either:
- Be the same file (this will make them mutually exclusive in playthroughs)
- Be one file with everything but the guitar stem, then one file with everything respectively. (this is how stems are intended to work in DELTARUNE)
	- To signal the game of the "no guitar" stem, your filename must include `"no_guit"` anywhere in it.
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
