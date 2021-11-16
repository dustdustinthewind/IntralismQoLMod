# Intralism Quality of Life Mod
A mod with a myriad of features and fixes that Oxy will never make.

Focus is primarily on editor features right now, though [I would like to touch up gameplay someday.](https://cdn.discordapp.com/attachments/646553696821444609/905530596632191066/91adfe01e7.png)

## FAQ
### How do I install the mod?
Click `Code > Download as Zip`. Right click Intralism in Steam and select `Manage > Browse Local Files`. Go into `Intralism_Data\Managed`. Copy the .dll files from the zip and paste them into the `Managed` folder. If it asks you to replace files say yes.

To patch with a newer version of the mod, you only need to download [Assembly-Csharp.dll](https://github.com/FlyingRabidUnicornPig/IntralismQoLMod/blob/main/Assembly-CSharp?raw=true). This may change in the future.

### How do I uninstall the mod?
Right click Intralism in Steam. Click `Properties`. Go to the `Local Files` tab and then click `Verify integrity of game files...`. This will restore Intralism to its current version.

### Can this mod ruin my editor or workshop map files?
There has been no features added that can drastically alter your files. Becareful loading maps with multiple BPMs in the description. If you try to open the BPM tool you will hang Intralism. If you save you will remove the characters (spaces, commas) between the BPMs.

### Can this mod get me banned?
I highly doubt it. Don't shove it in Oxy's face though.

### Isn't this against the terms of service?
As if that has stopped me, or others before. Oxy can feel free to take this down with a DMCA, that is totally in his right, and I will not complain if he does. I will still host the mod somewhere as long as I'm working on it.

## Features
### Current
- Config v3 maps do not encrypt (Encrypted maps can be resaved to be decrypted!)
- Gave Editor a Dark Theme
- The BPM tool uses colors for snaps (only for 1, 2, 3, 4, 6, 8, 12, 16 snaps, if you're using something else you're probably wrong)
- Editor sets BPM automatically if "BPM" is in the description. (Doesn't work with multiple BPMs)
- The current working BPM will be saved to the description.
- Navigation improvements: better caret, finer zoom controls
- The Discord RPC message for Editor will show the map you're working on
- Audio Waveform should be more consistent and accurate, in exchange for being a little slower than it used to be. Press skip if you don't care for the waveform and its limitations.

### Bugs list (mod bugs on top, vanilla bugs on bottom)
- Maps with multiple BPMs listed are not properly supported by the mod yet. You can hang Intralism into a crash, and overwrite your listed BPMs when you save if you're not careful!
- Audio Waveform in background doesn't delete when loading a new map. Vanilla Bug. Workaround: restart the editor. Seems to be one that stumped oxy as well, he tried several times to delete it)

### Working on
- Snap caret to BPM when scrolling.
- Calculate zoomless difficulty in "about"

### TO DO / Feature Wishlist (Feel free to [request](https://github.com/FlyingRabidUnicornPig/IntralismQoLMod/issues))
- Open last edited map
- Optimize Editor Events to not update offscreen (reduce lag with more objects + BPM + waveform, there's so many objects and they all move at once)
- Remove the 1-second bars in editor (we have enough things pointing up and down)
- Add buttons and settings for some features (disable waveforms, BPM Save button, turn off discord message, etc.)
- Edit the settings menu to make more sense
- Disable clicking on progress bar (no more accidentally going to the end of map)
- Change colors and sizes of events depending on type (imagine storyboard editing without a sea of green, starting/ending events being larger acting as bookmarks)
- Handle multiple BPMs and OFfsets
- Remake arcs editing to be closer to osu!m's editor in design.
- Sliding/stepped BPM tool? 👀
- Test Map from current time
- BPM Find tool (tap to the beat)
- Calculate and display difficulty on map select
- Toggle zooms in options (nerfs you on official maps so who cares bout modded rank submissions here lol)
- Keyboard shortcuts on main menu (one key press to editor for example)
- Change base dlls to non-obfuscated version (would probably save a lot of time and some headaches)
- Map Selector Optimizations and Improvements (caching?)
- Add better storyboard navigation/manipulation features (can use https://github.com/FlyingRabidUnicornPig/Intralism-Mapping-Assistant for reference)
- Decrease ram usage of storyboard images
- Skip the beginning/ending of a map
- Proper arc positioning
- Improved Zooms
- Timing Windows
- Custom player Speed
- Create a custom map config to allow more features for mappers/players (These would be backwards compat (save a v3 version for non-modded clients) and can be uploaded to the workshop)

Yes I'm using the Readme like I would a board, fuck you.
