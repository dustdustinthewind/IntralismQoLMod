Should only work with Windows version of the game.

# Intralism Quality of Life Mod
A mod with a myriad of [**features and fixes**](https://github.com/FlyingRabidUnicornPig/IntralismQoLMod#features) that Oxy will never make.

Focus is primarily on editor features right now, though [I would like to touch up gameplay someday.](https://cdn.discordapp.com/attachments/646553696821444609/905530596632191066/91adfe01e7.png)

![meme](https://cdn.discordapp.com/attachments/592268952265293824/910555214732488804/20211117071911_1.jpg)

## FAQ
### How do I install the mod?
Click [here](https://github.com/FlyingRabidUnicornPig/IntralismQoLMod/archive/refs/heads/main.zip) to download the current version. Right click Intralism in Steam and select `Manage > Browse Local Files`. Go into `Intralism_Data\Managed`. Copy the .dll files from the zip you downloaded and paste them into the `Managed` folder. If it asks you to replace files say yes.

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
- Config v3 maps and the save file **do not encrypt** (**Encrypted maps can be resaved to be decrypted!**)
- Gave Editor a **Dark Theme**
- The **BPM tool uses colors** for snaps (only for 1, 2, 3, 4, 6, 8, 12, 16 snaps, if you're using something else you're probably wrong)
- **Automatic BPM saving/loading** to and from description (Doesn't work properly with multiple BPMs)
- Navigation improvements:
  - Caret Doesn't slide
  - **Caret Snaps to BPM** (scroll faster by zooming out, playing the map, and/or holding shift)
  - **Refined Scroll Zoom** (Get much closer to the arcs without getting uncomfortably close like before)
  - Speed up to 2x or down to .125x (Press shift key or enable caps to step by .125x instead of .25x)
- **Audio Waveform should be more consistent and accurate**, in exchange for being a little slower than it used to be. Press skip if you don't care for the waveform and its limitations.
- **Playtest Map** button under the "Map" drop down menu. Replaces the "Exit" button (use `esc` to leave editor) Functional, but a work in progress.
- **Better Map Stats**. TODO: Button to copy map stats to map description.

### Gameplay
- Accuracy is now shown on all non-relax gamemodes (bug makes it squashed with lives atm)

### Misc
- **Map images will now compress** before being used as a texture. No more needing 30 gigs of ram to play an image sequencce storyboard. This does increase loading times. TODO: Give mappers control over compression.
- Downloaded **maps will display their difficulty** when hovered in map-select.
- Added a **backup feature to saves**, in case the mod or the game fucks things up.
- Press "O" while connecting to server to **Quickstart Offline Mode**
- **Several vanilla bugs have been squashed** (a never ending feat)
- **A couple easter eggs**

### Working on
- Copy Map Stats to map description
- Change zoom difficulty calculations (Thanks Deko for the new formula!)
- Change BPM/Snap Events (handle BPM through a new custom event rather than operating within the description. Would log errors on vanilla in console but that's it, no v4 needed.)
- Test Map from current time (test map implemented, from time not) (Reimplement as play testing *inside* the editor using playerbase?) (on the backburner)
- Custom Menu Music through skin folder (on the backburner)

### Bugs To Squash (mod bugs on top, vanilla bugs on bottom)
- Leaving the editor will take you to the map select on top of the main menu if you play tested. Mod Bug. **No Workaround**, besides taking longer to leave Intralism without alt+f4 or playing multi, this may actually be a useful bug for some lol.
- The "Map" drop down menu flashes and sometimes stays up while/after loading. Intetional Mod "Bug". **Workaround:** none needed. While this is currently intentional for reasons I do not have the energy nor space to explain, I'd rather this wasn't the case.
- Game Over screen is trying to update a null object every frame. Mod Bug. **No Workaround**
- Accuracy/Lives squashed. Mod Bug. **No Workaround**. Why is it so hard to modify UI elements?
- Untagged workshop maps don't pop up in map selector. Vanilla Bug. **No Workaround**
- Map Selector Sometimes pops up when entering the game. Vanilla Bug. **No Workaround:** If you know one, tell me.
- Editor overwrites custom values if they are out of range. Vanilla Bug. **Workaround:** Don't click "Apply" on events that have had their values set manually in config.txt.
- Highscore doesn't save the first time you play a new map. Vanilla Bug. **Workaround:** Fail the map with a positive score then start again.
- Rank updating can cause stutter during gameplay (is this still a bug? need to check/test). Vanilla Bug. **Workaround:** check console to wait for rank update before playing a map again
- Event Editor drop-down doesn't always position properly. Vanilla Bug. **Workaround:** Load a new arc, don't leave the drop down open while playing.


### TO DO / Feature Wishlist (Feel free to [request](https://github.com/FlyingRabidUnicornPig/IntralismQoLMod/issues))
- Open last edited map
- Custom Gamemode where you can set the speed before playing.
- Disable clicking on progress bar when event editor is up (no more accidentally going to the end of map when I try to click Apply)
- Less restriction in values available to select in Event Editor (replace sliders with text boxes or at least give them bigger, finer ranges)
- Create a custom map config to allow more features for modded clients. Workshop uploads would include a vanilla-compatible v3 config.
- Give mappers control over what images to compress (we don't have to compress and potentially ruin the quality of maps with few images)
- Proper arc positioning according to the music's time and not a spawner based on Time.deltaTime
- Optimize offscreen Editor elements
- Access the leaderboards for workshop maps
- Change colors and sizes of events depending on type (imagine storyboard editing without a sea of green, starting/ending events being larger acting as bookmarks)
- Remove the 1-second bars in editor (we have enough things pointing up and down)
- Mousewheel to control volume during gameplay
- BPM Find tool (tap to the beat)
- Video Player for storyboard
- Store raw texture data in map folder? With how small compression makes images, it may be reasonable to store them rather than loading/recompressing every time we load a map. This would significantly cut down loading times for maps with many images.
- Skip the beginning/ending of a map
- Fix negative zooms causing difficulty to be "Inifinte".
- Fix the replay system (Turns out there's a Replay Viewer in the code. Idk how well it works, it could be an artifact of a much older version of Intralism, but there's at least the base for one here.)
- Fix inaccuracies in Results Screen.
- Unlock the dev console
- Specific number of arcs, zooms, storyboard events, etc
- Add buttons and settings for some features (disable waveform generation, save BPMs, turn off discord rpc, etc.)
- Edit the settings menu to make more sense
- Add more editor themes
- Handle multiple BPMs and Offsets
- Sliding/stepped BPM tool?
- Remake arc-event editing to be closer to osu!m's editor in design.
- Toggle map zooms
- Keyboard shortcuts on main menu (one key press to editor for example)
- Map Selector Optimizations & Improvements (caching, faster loading, more maps, remember better)
- Add better storyboard navigation/manipulation features (can use https://github.com/FlyingRabidUnicornPig/Intralism-Mapping-Assistant for reference)
- Pause on esc press
- Improved Zooms, make them frame independent and add specific zoom types.
- Timing Windows
- Custom player Speed (with map speed acting as a modifer on top)
