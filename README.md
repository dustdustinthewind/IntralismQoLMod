Should only work with Windows version of the game.

# Intralism Quality of Life Mod
A mod with a myriad of [**features and fixes**](https://github.com/FlyingRabidUnicornPig/IntralismQoLMod#features) that Oxy will never make.

Focus is primarily on editor features right now, though [I would like to touch up gameplay best I can too.](https://cdn.discordapp.com/attachments/646553696821444609/905530596632191066/91adfe01e7.png)

## FAQ
### How do I install the mod?
Click [here](https://github.com/FlyingRabidUnicornPig/IntralismQoLMod/archive/refs/heads/main.zip) to download the current version. Right click Intralism in Steam and select `Manage > Browse Local Files`. Go into `Intralism_Data\Managed`. Copy all `.dll` files from the zip you downloaded and paste them into the `Managed` folder. Replace files, yes. The `qolmod` folder is optional.

To update your mod, you only need to download/paste the newest [Assembly-Csharp.dll](https://github.com/FlyingRabidUnicornPig/IntralismQoLMod/raw/main/Assembly-CSharp.dll). This could change in the future.

Updates happen frequently, so check often!

### How do I uninstall the mod?
Right click Intralism in Steam. Click `Properties`. Go to the `Local Files` tab and then click `Verify integrity of game files...`. This will restore Intralism to its current version. ***PLEASE NOTE***: Your save file will be considered "Corrupted" by intralism and deleted. Read the next question for assistance handling saves.

### What files does this mod mess with?
- This mod decrypts the save file found in `...\Intralism\Save`. **THIS WILL CAUSE INTRALISM TO DELETE YOUR SAVE IF YOU REVERT TO VANILLA.** If your first install was after version `0.6.3` you have nothing to worry about. Copy the `.bak_oldest` bakup file and change its extension to `.save`.
- If a save gets corrupted, try using the backups. Delete the faulty save and copy a backup. Change the backup copy's extension to `.save`. The `.bak_oldest` file was generated the first time you launched Intralism with mod version `0.6.3` or newer, and doesn't get overwritten by other backups. It is strongly recommended that you **do not delete this backup.**
- This mod uses custom map events that will throw console warnings on vanilla maps while playing and may cause a frame drop. This may be addressed by co-operation with the vanilla version to not run modded maps with a specific "Incompatible" tag (I've heard that has been suggested).

### Isn't this against Intralism's terms of service?
Update: [Oxy is OK with this project.](https://cdn.discordapp.com/attachments/429849391164030988/919666559071453214/4fcc2b930d.png)

### I mean can I get banned for using the mod?
There's no risk of VAC auto ban. It is highly unlikely to receive a manual ban by Intralism or Steam from using this mod.

## FEATURES
### EDITOR
- Config v3 **maps and the save file do not encrypt** (Encrypted maps can be resaved to be decrypted!)
- Gave Editor a **Dark Theme**
- **New Events**
  - [**BPM Events**](https://www.youtube.com/watch?v=uSNUuTWbvuk) for BPM automation (You can still use the old system if you prefer (somewhat buggy tho))
  - [**Player Position**](https://youtu.be/AVmlvf-fU0U)
  - [**Player Rotation**](https://www.youtube.com/watch?v=Wwh-CFWLpL8)
- **Changes to old events**
  - [**Added lerp-speed control for Distance events**](https://youtu.be/nfSsDREbh5c)
  - **Replaced sliders with text boxes** for Speed and Distance events
- [**Auto Animated Image Storyboard**](https://youtu.be/fzL2o3i5xrA)
- **Playtest Map** button under the "Map" drop down menu. Replaces the "Exit" button (use `esc` to leave editor)
- The **BPM tool uses colors** for snaps 1, 2, 3, 4, 6, 8, 12, and 16
- New Shortcuts:
  - `Home`/`End` to scroll to the start/end of the map
- **Removed "Complete Map" requirements**
- Navigation improvements:
  - **Caret Snaps to BPM** (scroll faster by zooming out, playing the map, and/or holding shift)
  - **Refined Scroll Zoom** (Get much closer to the arcs without getting uncomfortably close like before)
  - Playback speed up to 2x or down to .125x ([Press shift key or enable caps to step by .125x instead of .25x](https://youtu.be/llyDIod8bdo))
- **Better Map Stats** that can be pasted to the map's description
- **Audio Waveform should be more consistent and accurate**, in exchange for being a little slower than it used to be. Enable/Disable under "Gameplay" settings.
- **Increased Performance**
  - Events and images don't render when offscreen

### GAMEPLAY / STORYBOARD
- [**MASSIVE STORYBOARD OPTIMIZATIONS**](https://www.youtube.com/watch?v=sTeboyFxIj4) especially to audio-reading entities (suns, satellites, and particle emitters)
- **Accuracy is now shown** on all non-relax gamemodes
- **Quitting a map only plays the miss sound once now.** Protect your hearing!
- **Compression for Image events** You can manually set the compression for an image by changing the "Compress" value in the config files `levelResources` (use `true`/`false`. Vanilla maps that are saved in IQoL will use `null`). Use this on image-sequence maps or maps with many sprites/images to reduce the insane RAM/VRAM usage. Maps with only a few images don't take up a worrying amount of RAM/VRAM.
- **Autocompression for image-sequence maps**. If a map has at least 1 unique image for every second, the autocompresser will kick in. Most if not all Vanilla image-sequence maps get detected by this, and use significantly less RAM/VRAM than vanilla would in exchange for much longer loading times. You can rely on this autocompression for a modded image sequence map too.
- **Storyboard and zoom animations are "less frame-dependent"**. This means that maps should play very similarly on all modded clients, regardless of FPS. There is a slight, usually unnoticeable difference in animation between modded and vanilla.
- **Use any skin!** Set the skin you'd like in [`qolmod/skin.txt`](https://github.com/FlyingRabidUnicornPig/IntralismQoLMod/blob/main/qolmod/skin.txt)

### MISC
- Downloaded **maps will display their difficulty** when hovered in map-select.
- Difficulty Adjustments:
  - Zooms do not count towards diff calculation anymore.
- Added a **backup feature to saves**, in case it gets fucked up.
- Press "O" while connecting to server to **Quickstart Offline Mode** (works consistently if connection to steam is down/flakey, need to improve to work when connection to intralism is flakey)
- **Browse for non-tagged workshop maps** by selecting "NoTag" in the filter options (will ignore any other tags you've pressed)
- **New Settings** (feel free to [request](https://steamcommunity.com/id/DustDustInTheWind/) a personal QoL setting)
  - **"Gameplay"**
    - Disable editor using the map name in Discord RPC (for Dust)
    - Enable the Editor Waveform
    - Open Event Editor on editor startup. (for EDM)
    - Open last edited map on editor startup.
  - **Video**
    - FPS Lock using Unity's shitty built-in fps capper (may fuck with map timing. should be fixed when arc spawners use music time)
- **Many vanilla bugs have been squashed** (a never ending feat)
- **Several easter eggs**

### Bugs To Squash
- Mod Bug: Playtesting a lot in editor may cause a hang or crash when trying to leave the editor.
- Mod Bug: **MP3s do not play** **Workaround:** use vanilla, where they also don't work :/ (I actually have no clue how oxy actually got mp3s playing, this is a strangely unique scenario and I haven't been able to deobfuscate it yet. I will probably try to find a new solution instead of trying to understand the old solution.)
- Mod Bug: You can get your frame rate capped to 100 in some situations involving the waveform generation. **Workaround** restart the game.
- Mod Bug: Map Preview can be unreasonably laggy. **No Workaround**
- Mod Bug: Leaving the editor will take you to the map select on top of the main menu if you play tested. (related to vanilla map select bug) **No Workaround**
- May be fixed: It is possible to make a ["blank"](https://cdn.discordapp.com/attachments/592268952265293824/922244562657902662/bfa5ddd08a.png) event that breaks the editor. **Workaround:** Search for `"data": []` in the map config file and delete the offending event.
- Intentional Mod "Bug": The "Map" drop down menu flashes and sometimes stays up while/after loading. I'd rather this wasn't the case.
- Vanilla Bug: Map Selector Sometimes pops up on game startup. (related to playtest mod bug) **Workaround:** Don't force close intralism after opening (but not closing) the map selector.
- Vanilla Bug: Map Selector always goes to page 1 of the Editor tab when loading maps.
- Vanilla Bug: Highscore doesn't save the first time you play a new map. **Workaround:** Fail the map with a positive score then start again.
- Vanilla Bug: Rank updating can cause stutter during gameplay (is this still a bug? need to check/test). **Workaround:** check console to wait for rank update before starting a map again
- Vanila Bug: Event Editor drop-down doesn't always position properly, sometimes not even appearing on screen. **Workaround:** Scroll to a new event, click Apply to refresh, and try not to leave the drop down open while playing the song.

### "High Priority" TODO
- Map Backup
- Make Difficulty calculation ignore events after MapEnd
- Bug Fixes and Optimizations
- Endlessly updating the Readme
- Custom Menu Music through skin folder

### TO DO / Feature Wishlist (Feel free to [request](https://steamcommunity.com/id/DustDustInTheWind/) or [here](https://github.com/FlyingRabidUnicornPig/IntralismQoLMod/issues))
- Color palette for storyboard events
- Open map folder button in editor
- Change the crosshair to a transparent version of your current view model, a 3D crosshair that matches the skin you're using and might properly represent the nonexistant "judgement line" at z0 compared to a fucking 2D image.
- Custom workshop tags
- Multi-storyboard-object spawner event (spawn x number of an object with a shared id (sun1, sun2, sun3, etc))
- Mirror-storyboard event (an event that handles multiple objects mirrored over a specified angle/other parameters)
- Custom Gamemode where you can set the speed before playing.
- Disable clicking on progress bar when event editor is up (no more accidentally going to the end of map when I try to click Apply)
- Give mappers control over what images to compress (we don't have to compress and potentially ruin the quality of maps with few images)
- Change arc spawner to use music time instead of Time.deltaTime
- Change arc movement to adjust based on music time instead of a set speed
- Access the leaderboards of workshop maps (IIRC every workshop map has a leaderboard that can be used)
- Change colors and sizes of events depending on type (imagine storyboard editing without a sea of green, starting/ending events being larger acting as bookmarks)
- Remove the 1-second bars in editor (nts: 💡 create a new gameobject rather than modifying the current one)
- Mousewheel to control volume during gameplay
- BPM Find tool (tap to the beat)
- Video Player for storyboard?
- Skip the beginning/ending of a map
- List the specific number of arcs, zooms, storyboard events, etc
- Add more editor themes
- Disable Zooms setting
- Keyboard shortcuts in main menu (one key press to editor for example)
- Map Selector Optimizations & Improvements (caching, faster loading, more maps, remember better, fix lag)
- Add better storyboard navigation/manipulation features (can use https://github.com/FlyingRabidUnicornPig/Intralism-Mapping-Assistant for reference)
- Pause on esc press
