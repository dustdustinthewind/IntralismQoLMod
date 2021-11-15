# Intralism Quality of Life Mod
A mod with a myriad of features and fixes that Oxy will never make.

Focus is primarily on editor features right now, though [I would like to touch up gameplay someday.](https://cdn.discordapp.com/attachments/646553696821444609/905530596632191066/91adfe01e7.png)

## FAQ
### How do I install the mod?
Click `Code > Download as Zip`. Right click Intralism in Steam and select `Manage > Browse Local Files`. Go into `Intralism_Data\Managed`. Copy the .dll files from the zip and paste them into the `Managed` folder. If it asks you to replace files say yes.

### How do I uninstall the mod?
Right click Intralism in Steam. Click `Properties`. Go to the `Local Files` tab and then click `Verify integrity of game files...`. This will restore Intralism to its current version.

### Can this mod ruin my editor or workshop map files?
There has been no features added that can drastically alter your files. Currently, the most that can happen is your maps will receive a "BPM 120" at the end of the description when you save.

### Isn't this against the terms of service?
As if that has stopped me, or Def, or others before. Oxy can feel free to take this down with a DMCA, that is totally in his right, and I will not complain if he does. I will still host the mod somewhere as long as I'm working on it.

## Features
### Known Bugs
- Newly placed arcs don't get selected by the Event Editor (Maybe be a vanilla bug, will fix regardless it's shitty.)
- Either Copying or Pasting is screwed up. You can only paste 1 arc even if you tried to copy more.
- Maps with multiple BPMs listed are not properly supported by the mod yet. You can hang Intralism into a crash, and overwrite your listed BPMs if you're not careful!

### Current
- Config v3 maps do not encrypt (Encrypted maps can be resaved to be decrypted!)
- Editor has dark background
- Current event is highlighted in Editor
- The editor will attempt to set the BPM if a map has "BPM" in the description
- The editor automatically finds BPM Offset from first arc in map (may crash if you have a 0 arc map)
- The BPM will be saved to the description of the map.
- The editor caret no longer slides
- The Discord RPC message for Editor will show the map you're working on
- Color-coded BPM tool
- Improved Editor-zoom controls (more fidelity and removed unneded ranges)

### Working on
- Copy/Paste Bug (Copy/paste functions are unchanged, what could be affecting this? how are my changes be fucking with it?)
- Readd the editor audio waveform as a toggleable setting
- Increase accuracy of audio waveform (and/or allow users to select accuracy. ~~This will increase the time it takes for a waveform to load, could look into saving the data through caching or other means~~ no oxy is just bad at coding ofc)

### TO DO / Feature Wishlist (Feel free to [request](https://github.com/FlyingRabidUnicornPig/IntralismQoLMod/issues))
- Scroll snap to BPM tool
- Open last edited map
- Remove the 1-second bars in editor (we have enough things pointing up and down)
- Add toggles for some features (turn on/off sliding caret, BPM Save button, turn off discord message, etc.)
- Disable clicking on progress bar (no more accidentally going to the end of map)
- Handle multiple BPMs and OFfsets
- Test Map from current time
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
