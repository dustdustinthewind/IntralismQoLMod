# Intralism Quality of Life Mod
A mod with a myriad of features and fixes that Oxy will never make.

Focus is primarily on editor features right now, though [I would like to touch up gameplay someday.](https://cdn.discordapp.com/attachments/646553696821444609/905530596632191066/91adfe01e7.png)

## FAQ
### How do I install the mod?
Click `Code > Download as Zip`. Right click Intralism in Steam and select `Manage > Browse Local Files`. Go into `Intralism_Data\Managed`. Copy the .dll files from the zip and paste them into the `Managed` folder. If it asks you to replace files say yes.

To update your mod, you only need to copy/paste the newest [Assembly-Csharp.dll](https://github.com/FlyingRabidUnicornPig/IntralismQoLMod/blob/main/Assembly-CSharp?raw=true). This may change in the future.

### How do I uninstall the mod?
Right click Intralism in Steam. Click `Properties`. Go to the `Local Files` tab and then click `Verify integrity of game files...`. This will restore Intralism to its current version.

### Can this mod ruin my editor or workshop map files?
There has been no features added that can drastically alter your files. The BPM tool will automatically write/read from your description, but it shouldn't cause any issues unless you're trying to break it.

### Isn't this against the terms of service?
As if that has stopped me, or others before. Oxy can feel free to take this down with a DMCA, that is totally in his right. However, I will still host the mod somewhere as long as I'm working on it.

### I mean will I get banned?
I highly doubt it. Don't shove it in Oxy's face though. There is no risk of Steam ban or VAC.

## Features
### Editor
- Config v3 maps do not encrypt (Encrypted maps can be resaved to be decrypted!)
- Gave Editor a Dark Theme
- The BPM tool uses colors for snaps (only for 1, 2, 3, 4, 6, 8, 12, 16 snaps, if you're using something else you're probably wrong)
- Automatic BPM saving/loading to and from description (Doesn't work properly with multiple BPMs)
- Navigation improvements: better caret, finer zoom controls
- The Discord RPC message for Editor will show the map you're working on
- Audio Waveform should be more consistent and accurate, in exchange for being a little slower than it used to be. Press skip if you don't care for the waveform and its limitations.

### Misc
- Intralism now compresses textures pulled from images. No more needing 30 gigs of ram to play an image sequencce storyboard. This does increase loading times.

### Working on
- Test Map from current time
- Add Shift key modifier to BPM scroll to scroll faster.

### Bugs To Squash (mod bugs on top, vanilla bugs on bottom)
- There's a "Play Test Map" button that doesn't do anything yet. Mod Bug. The first part of an upcoming feature.
- The "Map" drop down menu flashes while loading the map. Intetional Mod "Bug". Workaround: none needed. While this is currently intentional for reasons I do not have the energy nor ability to explain, I'd rather this wasn't the case.
- Audio Waveform in background doesn't delete when loading a new map. Vanilla Bug. Workaround: restart the editor. Seems to be one that stumped oxy as well, he tried several times to delete it)
- Event Editor drop-down doesn't always position properly. Vanilla Bug. Workaround: Load a new arc, don't leave the drop down open while playing.
- Editor overwrites custom values if they are out of range. Vanilla Bug. Workaround: Don't apply changes to events with values set manually in config.txt.
- Highscore doesn't save the first time you play a new map. Vanilla Bug. Workaround: Stop the map before starting proper.


### TO DO / Feature Wishlist (Feel free to [request](https://github.com/FlyingRabidUnicornPig/IntralismQoLMod/issues))
- Open last edited map
- Optimize Editor Events to not update offscreen (reduce/remove lag that comes from many events + BPM snaps + waveform, there's so many objects and they all move at once...)
- Remove the 1-second bars in editor (we have enough things pointing up and down)
- Add buttons and settings for some features (disable waveforms, BPM Save button, turn off discord message, etc.)
- Edit the settings menu to make more sense
- Disable clicking on progress bar (no more accidentally going to the end of map)
- Change colors and sizes of events depending on type (imagine storyboard editing without a sea of green, starting/ending events being larger acting as bookmarks)
- Handle multiple BPMs and OFfsets
- Less restriction in values available to select in Event Editor (replace sliders with text boxes?)
- Remake arcs editing to be closer to osu!m's editor in design.
- Sliding/stepped BPM tool?
- BPM Find tool (tap to the beat)
- Store raw texture data in map folder? With how small compression makes images, it may be reasonable to store them rather than loading/recompressing every time we load a map. This would significantly cut down loading times for maps with many images.
- Calculate and display difficulty on map select
- Disable/Enable map zooms
- Keyboard shortcuts on main menu (one key press to editor for example)
- Change base dlls to non-obfuscated version (would probably save a lot of time and some headaches)
- Map Selector Optimizations and Improvements (caching?)
- Add better storyboard navigation/manipulation features (can use https://github.com/FlyingRabidUnicornPig/Intralism-Mapping-Assistant for reference)
- Skip the beginning/ending of a map
- Proper arc positioning
- Improved Zooms
- Timing Windows
- Custom player Speed
- Create a custom map config to allow more features for mappers/players (These would be backwards compat (save a v3 version for non-modded clients) and can be uploaded to the workshop)

Yes I'm using the Readme like I would a board, fuck you.
