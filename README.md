Should only work with Windows version of the game.

# Intralism Quality of Life Mod
A mod with a myriad of [**features and fixes**](https://github.com/FlyingRabidUnicornPig/IntralismQoLMod#features) that Oxy will never make.

Focus is primarily on editor features right now, though [I would like to touch up gameplay best I can too.](https://cdn.discordapp.com/attachments/646553696821444609/905530596632191066/91adfe01e7.png)

![meme](https://cdn.discordapp.com/attachments/592268952265293824/910555214732488804/20211117071911_1.jpg)

## FAQ
### How do I install the mod?
Click [here](https://github.com/FlyingRabidUnicornPig/IntralismQoLMod/archive/refs/heads/main.zip) to download the current version. Right click Intralism in Steam and select `Manage > Browse Local Files`. Go into `Intralism_Data\Managed`. Copy all files from the zip you downloaded and paste them into the `Managed` folder. Replace files, yes.

To update your mod, you usually only need to download/paste the newest [Assembly-Csharp.dll](https://github.com/FlyingRabidUnicornPig/IntralismQoLMod/raw/main/Assembly-CSharp.dll). As of vers `v0.9.0` there is a `qolmod` folder, it is entirely optional at the moment.

Updates happen frequently, check daily if you wish to stay up to date!

### How do I uninstall the mod?
Right click Intralism in Steam. Click `Properties`. Go to the `Local Files` tab and then click `Verify integrity of game files...`. This will restore Intralism to its current version. ***PLEASE NOTE***: Your save file will be considered "Corrupted" by intralism and deleted. Read the next question for assistance handling saves.

### What files does this mod mess with?
- This mod uses a custom event called "SetBPM", this will throw errors on vanilla maps while playing (should not crash editor or gameplay) and may cause a frame drop. I have a fix in mind.
- This mod decrypts the save file found in `...\Intralism\Save`. **THIS WILL CAUSE INTRALISM TO DELETE YOUR SAVE IF YOU REVERT TO VANILLA.** If your first install was after version `0.6.3` you have nothing to worry about. Find the `.bak_oldest` bakup file and change its extension to `.save`. If you first installed the mod before this version, you will need to wait for a future version where I remedy this issue with a `.bak_vanilla` file to use. 
- If a save gets corrupted, try using the backups. Delete the faulty save and copy a backup. Change the backup copy's extension to `.save`. The `.bak_oldest` file was generated the first time you launched Intralism with mod version `0.6.3` or newer, and doesn't get overwritten by other backups. It is strongly recommended that you **do not delete this backup.**

### Isn't this against Intralism's terms of service?
Update: [Oxy is OK with this project.](https://cdn.discordapp.com/attachments/429849391164030988/919666559071453214/4fcc2b930d.png)

### I mean can I get banned for using the mod?
I highly doubt it. Even if you're banned by the Intralism webserver, the ban checks are handled by the local client, easy for hackers but not normies to bypass. This mod removes (most if not all) those checks; enjoy your freedom.

There is no risk of being auto banned by Steam or VAC.

## FEATURES
### EDITOR
- Config v3 **maps and the save file do not encrypt** (**Encrypted maps can be resaved to be decrypted!**)
- Gave Editor a **Dark Theme**
- [**BPM Events**](https://www.youtube.com/watch?v=uSNUuTWbvuk) for BPM automation! (a little guggy, but functional)
- **Playtest Map** button under the "Map" drop down menu. Replaces the "Exit" button (use `esc` to leave editor) Functional, but a work in progress.
- The **BPM tool uses colors** for snaps 1, 2, 3, 4, 6, 8, 12, and 16
- Navigation improvements:
  - Caret Doesn't slide
  - **Caret Snaps to BPM** (scroll faster by zooming out, playing the map, and/or holding shift)
  - **Refined Scroll Zoom** (Get much closer to the arcs without getting uncomfortably close like before)
  - Speed up to 2x or down to .125x ([Press shift key or enable caps to step by .125x instead of .25x](https://youtu.be/llyDIod8bdo))
- **Replaced Sliders with text boxes** for Speed and Distance events
- **Better Map Stats that can be pasted to the map's description**
- **Audio Waveform should be more consistent and accurate**, in exchange for being a little slower than it used to be. Press skip if you don't care for the waveform and its limitations.
- **Increased Performance**

### GAMEPLAY / STORYBOARD
- **MASSIVE STORYBOARD OPTIMIZATIONS** especially to audio-reading entities (suns, satellites, and particle emitters) [video showcase](https://www.youtube.com/watch?v=sTeboyFxIj4)
- **Map images will now compress** before being used as a texture. No more needing 30 gigs of ram to play an image sequence storyboard. This does increase loading times. TODO: Give mappers control over compression.
- **Storyboard and zoom animations are less frame-dependent**. This means that maps should play very similarly on all modded clients. This alters the style between version, i.e. playing a vanilla map on a modded client will "feel" different, and vice versa, a modded map will feel different on vanilla.
- **Use any skin!** Set the skin you'd like in [`qolmod/skin.txt`](https://github.com/FlyingRabidUnicornPig/IntralismQoLMod/blob/main/qolmod/skin.txt)
- Accuracy is now shown on all non-relax gamemodes

### MISC
- Downloaded **maps will display their difficulty** when hovered in map-select.
- Difficulty Adjustments:
  - Zooms outside of 4-40 get treated as 4 or 40, to reduce diff abuse at extremely low or extremely high values. (potentially nerfs the max rank score you can submit)
- Added a **backup feature to saves**, in case it gets fucked up.
- Press "O" while connecting to server to **Quickstart Offline Mode** (works consistently if connection to steam is down/flakey)
- **Browse for non-tagged maps** by selecting "NoTag" in the filter options (will ignore any other tags you've pressed)
- Added extra settings
- **Many vanilla bugs have been squashed** (a never ending feat)
- **A couple easter eggs**

### Working on
- Test Map from current time (test map implemented, from time not) (nts: Reimplement as play testing *inside* the editor using playerbase?)
- Optimizations
- Settings Menu Additions/Revisions
- Make Difficulty calculation ignore events after MapEnd
- Custom Menu Music through skin folder

### Bugs To Squash
- Mod Bug: **MP3s do not play** **Workaround:** use vanilla, where they also don't work :/
- Mod Bug: **Disable storyboard** gets overwritten by the new discord editor setting when you launch the settings menu for the first time (i.e. when you launch the menu) **Workaround:** Click "Disable Storyboard" to your preference when you launch the game.
- Mod Bug: Leaving the editor will take you to the map select on top of the main menu if you play tested. **No Workaround**
- Intentional Mod "Bug": The "Map" drop down menu flashes and sometimes stays up while/after loading. I'd rather this wasn't the case.
- Mod Bug: Assorted debug spam that could effect performance. **Workaround** Click the "report a bug" button on the main menu and [let me know!](https://steamcommunity.com/id/DustDustInTheWind/)
- Vanilla Bug: Map Selector Sometimes pops up when entering the game. **Workaround:** Don't force close intralism after opening (but not closing) the map selector.
- Vanilla Bug: Editor overwrites custom values if they are out of range.**Workaround:** Don't click "Apply" on events that have had their values set manually in config.txt.
- Vanila Bug: Highscore doesn't save the first time you play a new map. **Workaround:** Fail the map with a positive score then start again.
- Vanilla Bug: Rank updating can cause stutter during gameplay (is this still a bug? need to check/test). **Workaround:** check console to wait for rank update before playing a map again
- Vanila Bug: Event Editor drop-down doesn't always position properly. **Workaround:** Scroll to a new arc, don't leave the drop down open while playing.

### TO DO / Feature Wishlist (Feel free to [request](https://steamcommunity.com/id/DustDustInTheWind/) or [here](https://github.com/FlyingRabidUnicornPig/IntralismQoLMod/issues))
- Change the crosshair to a transparent version of your current view model, a 3D crosshair that matches the skin you're using and will properly represent the nonexistant "judgement line" at z0 compared to a fucking 2D image.
- Open last edited map
- Custom workshop tags
- Custom FPS Lock slider setting
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
- Video Player for storyboard?
- Skip the beginning/ending of a map
- Fix the replay system (Turns out there's a Replay Viewer in the code. Idk how well it works, it could be an artifact of a much older version of Intralism, but there's at least the base for one here.)
- Fix inaccuracies in Results Screen.
- Unlock the dev console
- List the number of arcs, zooms, storyboard events, etc
- Add more editor themes
- Remake arc-event editing to be closer to osu!m's editor in design?
- Toggle map zooms
- Keyboard shortcuts on main menu (one key press to editor for example)
- Map Selector Optimizations & Improvements (caching, faster loading, more maps, remember better)
- Add better storyboard navigation/manipulation features (can use https://github.com/FlyingRabidUnicornPig/Intralism-Mapping-Assistant for reference)
- Pause on esc press
- Timing Windows
- Custom player Speed (with map speed acting as a modifer on top)
