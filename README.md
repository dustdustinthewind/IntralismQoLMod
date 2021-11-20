# Intralism Quality of Life Mod
A mod with a myriad of features and fixes that Oxy will never make.

Focus is primarily on editor features right now, though [I would like to touch up gameplay someday.](https://cdn.discordapp.com/attachments/646553696821444609/905530596632191066/91adfe01e7.png)

![meme](https://cdn.discordapp.com/attachments/592268952265293824/910555214732488804/20211117071911_1.jpg)

## FAQ
### How do I install the mod?
Click `Code > Download as Zip`. Right click Intralism in Steam and select `Manage > Browse Local Files`. Go into `Intralism_Data\Managed`. Copy the .dll files from the zip and paste them into the `Managed` folder. If it asks you to replace files say yes.

To update your mod, you only need to copy/paste the newest [Assembly-Csharp.dll](https://github.com/FlyingRabidUnicornPig/IntralismQoLMod/raw/main/Assembly-CSharp.dll). This may change in the future.

### How do I uninstall the mod?
Right click Intralism in Steam. Click `Properties`. Go to the `Local Files` tab and then click `Verify integrity of game files...`. This will restore Intralism to its current version.

### Can this mod ruin my files?
This mod should not mess with your files in unwanted ways. However of note:
- The BPM tool will automatically write/read from your description, but it shouldn't cause any issues unless you're trying to break it. Multi-BPM/offset mapping is not supported yet.
- This mod decrypts the save file found in `...\Intralism\Save`. While I'm pretty sure I correctly implemented this feature, there is very much the chance that something could go wrong. For this and other reasons, I have implemented a feature that keeps three save backups in the same folder as your save data. If a save gets corrupted, try using the backups. Delete the faulty save and change the extenion of the backup you want to use to `.save`. The `.bak_oldest` file was generated the first time you launched Intralism with mod version `0.6.3` or newer, and doesn't get overwritten by other backups.

### Isn't this against Intralism's terms of service?
As if that has stopped me, or others before. Oxy can feel free to take this down with a DMCA, that is totally in his right. However, I will still host the mod somewhere as long as I'm working on it.

### I mean will I get banned for using the mod?
I highly doubt it. Don't shove it in Oxy's face though. There is no risk of Steam or VAC ban.

## Features
### Editor
- Config v3 maps and the save file do not encrypt (Encrypted maps can be resaved to be decrypted!)
- Gave Editor a Dark Theme
- The BPM tool uses colors for snaps (only for 1, 2, 3, 4, 6, 8, 12, 16 snaps, if you're using something else you're probably wrong)
- Automatic BPM saving/loading to and from description (Doesn't work properly with multiple BPMs)
- Navigation improvements: better caret, finer zoom controls
- The Discord RPC message for Editor will show the map you're working on
- Audio Waveform should be more consistent and accurate, in exchange for being a little slower than it used to be. Press skip if you don't care for the waveform and its limitations.
- Playtest Map button under the "Map" drop down menu. Only launches from start of map, still work in progress.

### Gameplay
- Accuracy is now shown on all non-relax gamemodes.

### Misc
- Loaded textures (skin, storyboard, map icons) will now compress. No more needing 30 gigs of ram to play an image sequencce storyboard. This does increase loading times.
- Downloaded maps will display their difficulty when hovered in map-select
- Added a backup feature to the save data, in case the game or the mod fucks things up.
- Several vanilla bugs have been squashed (a never ending feat)

### Working on
- Test Map from current time

### Bugs To Squash (mod bugs on top, vanilla bugs on bottom)
- Level Select takes longer to load due to compression be aplied there. Mod Bug. Workaround: None.
- Trying to exit the map while the waveform is generating will not close the editor, but instead stops the waveform generation. Workaround: Try exiting again. Will be fixed when wave form generation is in the settings rather than a dialog box.
- If you play tested in the Editor, leaving the editor will take you to the map select on top of the main menu. Mod Bug. Workaround: None, besides taking longer to leave Intralism without alt+f4 or playing multi, this may actually be a useful bug for some lol.
- The "Map" drop down menu flashes while loading the map. Intetional Mod "Bug". Workaround: none needed. While this is currently intentional for reasons I do not have the energy nor space to explain, I'd rather this wasn't the case.
- Lives do not display on non-hardcore gamemodes. Mod Bug. No Workaround: Do people care about lives?
- Audio Waveform in background doesn't delete when loading a new map. Vanilla Bug. Workaround: restart the editor. Seems to be one that stumped oxy as well, he tried several times to delete it)
- Event Editor drop-down doesn't always position properly. Vanilla Bug. Workaround: Load a new arc, don't leave the drop down open while playing.
- Editor overwrites custom values if they are out of range. Vanilla Bug. Workaround: Don't click "Apply" on events that have had their values set manually in config.txt.
- Highscore doesn't save the first time you play a new map. Vanilla Bug. Workaround: Stop the map before starting proper.


### TO DO / Feature Wishlist (Feel free to [request](https://github.com/FlyingRabidUnicornPig/IntralismQoLMod/issues))
- Open last edited map
- Fix/Make accessible the replay system (Turns out theirs a Replay Viewer in the code. Idk how well it works, it could be an artifact of an older version, but there's at least the base for one here.)
- Unlock the dev console
- Fix inaccuracies in Results Screen.
- Key button to skip connecting to shoddy russian servers
- Optimize Editor Events to not update offscreen (reduce/remove lag that comes from many events + BPM snaps + waveform, there's so many objects and they all move at once...)
- Remove the 1-second bars in editor (we have enough things pointing up and down)
- Add buttons and settings for some features (disable waveforms, BPM Save button, turn off discord message, etc.)
- Edit the settings menu to make more sense
- Add more editor themes
- Disable clicking on progress bar (no more accidentally going to the end of map)
- Change colors and sizes of events depending on type (imagine storyboard editing without a sea of green, starting/ending events being larger acting as bookmarks)
- Handle multiple BPMs and OFfsets
- Less restriction in values available to select in Event Editor (replace sliders with text boxes?)
- Remake arcs editing to be closer to osu!m's editor in design.
- Sliding/stepped BPM tool?
- BPM Find tool (tap to the beat)
- Store raw texture data in map folder? With how small compression makes images, it may be reasonable to store them rather than loading/recompressing every time we load a map. This would significantly cut down loading times for maps with many images.
- Give mappers control over what images compress (we don't have to compress and potentially ruin the quality of map icons or maps with 1 Image)
- Disable/Enable map zooms
- Keyboard shortcuts on main menu (one key press to editor for example)
- Map Selector Optimizations and Improvements (caching?)
- Add better storyboard navigation/manipulation features (can use https://github.com/FlyingRabidUnicornPig/Intralism-Mapping-Assistant for reference)
- Skip the beginning/ending of a map
- Proper arc positioning according to the music's time and not a spawner with a unity timer
- Improved Zooms, make them not frame-rate dependent and add specific zoom types.
- Timing Windows
- Custom player Speed (with map speed acting as a modifer on top)
- Create a custom map config to allow more features for mappers/players (These would be backwards compat (save a v3 version for non-modded clients) and can be uploaded to the workshop)

Yes I'm using the Readme like I would a board, fuck you.
