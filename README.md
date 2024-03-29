Should only work with Windows version of the game.

[Currently busy dumping Intralism](https://github.com/FlyingRabidUnicornPig/).  Will return with updates to this repo when I finish.

[Please consider donating to my ko-fi.](https://ko-fi.com/dustdust)

# Intralism Quality of Life Mod
A mod with a myriad of [**features and fixes**](https://github.com/FlyingRabidUnicornPig/IntralismQoLMod#features) to improve mapping and gameplay.

## FAQ
### How do I install the mod?
Click [here](https://github.com/FlyingRabidUnicornPig/IntralismQoLMod/archive/refs/heads/main.zip) to download the current version. Right click Intralism in Steam and select `Manage > Browse Local Files`. Go into `Intralism_Data\Managed`. Copy all `.dll` files from the zip you downloaded and paste them into the `Managed` folder. Replace files, yes. The `qolmod` folder is optional.

### How do I update the mod?
To update your mod, you only need to download/paste the newest [Assembly-Csharp.dll](https://github.com/FlyingRabidUnicornPig/IntralismQoLMod/raw/main/Assembly-CSharp.dll). Same folder, same thing, replace files, yes. The update process could change in the future.

[Dump](https://github.com/FlyingRabidUnicornPig/IQoLDecompiled) version can be found [here](https://github.com/FlyingRabidUnicornPig/IQoLDecompiled/raw/main/Assembly-CSharp.dll). Check out the [feature list here](https://github.com/FlyingRabidUnicornPig/IQoLDecompiled#new-features-for-release) I RECOMMEND BACKING UP YOUR MAPS (preferably outside of Intralism's files). I am tweaking/optimizing the entire code, not just dumping, something very bad could happen.

### How do I uninstall the mod?
Right click Intralism in Steam. Click `Properties`. Go to the `Local Files` tab and then click `Verify integrity of game files...`. This will restore Intralism to its current version. ***PLEASE NOTE***: Your save file will be considered "Corrupted" by intralism and deleted. Read the next question for assistance handling saves.

### What important things does this mod mess with?
- This mod decrypts the save file found in `...\Intralism\Save`. **THIS WILL CAUSE INTRALISM TO DELETE YOUR SAVE IF YOU REVERT TO VANILLA.** To fix this, close Intralism, delete the `.save` file, duplicate the `.bak_oldest` bakup file but change its extension to `.save`. 
- If a save gets corrupted, try using the backups. Delete the faulty save and copy a backup. Change the backup copy's extension to `.save`. The `.bak_oldest` file was generated the first time you launched the mod. It is strongly recommended that you **do not delete the .bak_oldest file, as it is vanilla-compatible.**
- This mod creates custom map events that will throw console warnings when played on vanilla, and may cause frame drops. Any new events will trigger this, modified vanilla events (old events with new settings) will not trigger a console warning. If you upload a map with modded events besides BPM, I recommend you leave a notice on the map thumbnail ([example](https://steamuserimages-a.akamaihd.net/ugc/1817764136694754642/3A7615BACE215E783C82A9BC3FE40B37E1F4845C/?imw=5000&imh=5000&ima=fit&impolicy=Letterbox&imcolor=%23000000&letterbox=false)). I may be able to make this nicer for vanilla users in the future.
- This mod has adjusted the difficulty calculation. At the moment the most it does is nerf difficulty, meaning ranked scores will also get nerfed. I recommend you play on vanilla if you wish to play ranked, especially considering I intend to remove vanilla rank submitting someday.

### Can I get banned for using the mod?
There's no risk of VAC auto ban. You are almost certainly safe from Steam or Intralism bans. There's always a chance, but I doubt they care. Thus far, no one has been banned for using the mod.

Update: [Oxy has given his blessing to this project.](https://cdn.discordapp.com/attachments/429849391164030988/919666559071453214/4fcc2b930d.png)

## FEATURES
### EDITOR
- **Maps and the save file do not encrypt** (Encrypted maps can be resaved to be decrypted!)
- Gave Editor a **Dark Theme**
- **New Events**
  - [**BPM Events**](https://www.youtube.com/watch?v=uSNUuTWbvuk) for BPM automation (You can still use the old system if you prefer (somewhat buggy tho))
  - [**Player Position**](https://youtu.be/AVmlvf-fU0U)
  - [**Player Rotation**](https://www.youtube.com/watch?v=Wwh-CFWLpL8)
- **Changes to old events**
  - [**Added lerp-speed control for Distance events**](https://youtu.be/nfSsDREbh5c)
  - **Replaced sliders with text boxes** for Speed and Distance events
  - [**Arc selector doesn't require scrolling**](https://cdn.discordapp.com/attachments/592268952265293824/945025806256726096/unknown.png)
- [**Auto Animated Image Storyboard**](https://youtu.be/fzL2o3i5xrA)
- **Playtest Map** button under the "Map" drop down menu. Replaces the "Exit" button (use `esc` to leave editor)
  - You can also **press your quick-restart button to start playtesting from the start of the map**.
- The **BPM tool uses colors** for snaps 1, 2, 3, 4, 6, 8, 12, and 16
- New Shortcuts:
  - `Home`/`End` to scroll to the start/end of the map
  - Hold `Shift` to modify snap-scroll/slomo step.
  - Press your quick-restart key to playtest from the start of the map
  - Hold `Ctrl` when clicking "Playtest" to playtest with "Infinite" lives.
- **Removed "Complete Map" requirements**
- Prettify Map Files, resave your map [to make maps more readable](https://cdn.discordapp.com/attachments/452707001399509003/984158364235882536/unknown.png)
- **Compression for Image Resources** You can manually set the compression for an image by changing the "Compress" value in the config file's `levelResources` (use `true`/`false`. Vanilla maps that are resaved in IQoL use `null`). In general, set animated images (movie to image-sequence) to true. If you reaching 100 or more high quality images, you should consider compressing those as well. If you only have one or two images, or are playing a small animated loop, compression is probably not needed. To check how much RAM a map uses, use task manager and add Intralism's RAM usage to your GPU's VRAM usage (check performance tab), *after* a map is finished loading. That value gives you a good estimate for the minimum total RAM needed to run the map.
- **Batch import image resources.** If the file system finds more than 1 image with the same header name (e.g. `fileNameXXX` where `X`s are numbers), you can batch import all of them at once. Note: Batched images are automatically tagged to compress. Non-batched images are tagged to not compress.
  - If you change the `Image FPS` text box, the import process will also automatically create the events for you.
  - Use the `Sequence Offset` box to change when these events start.
- Navigation improvements:
  - **Caret Snaps to BPM** (scroll faster by zooming out, if the song is playing, and/or holding shift)
  - **Refined Scroll Zoom** (Don't snap uncomfortably close to arcs when zooming in anymore)
  - Playback speed up to 2x or down to .125x ([Press shift key or enable caps to step by .125x instead of .25x](https://youtu.be/llyDIod8bdo))
- **User-Relevant Map Stats** that can be pasted to the description.
- **Audio Waveform should be more consistent and accurate**, in exchange for being a little slower than it used to be. Enable/Disable under "Gameplay" settings.
- **Increased Performance**
  - Events and images don't render when offscreen
  - The grey time-bar consists of only 3 objects instead of 3 objects for every second in the song.
  - BPM Grid only draws once, follows active track

### GAMEPLAY / STORYBOARD
- [**MASSIVE OPTIMIZATIONS FOR AUDIO-READING OBJECTS**](https://www.youtube.com/watch?v=sTeboyFxIj4) (Suns, Satellites, and Particle Emitters will share audio data with each other, instead of refreshing the same audio data of that frame for every single object)
- **Accuracy is now shown** on all non-relax gamemodes
- **Quitting a map only plays the miss sound once.** Protect your hearing!
- **Less Frequent Rank Refresh** Ranks only refresh after a score submit if 10 minutes have passed since the last submission. [This is a quick and dirty solution to handle issues of the current "Rank" Refresh system](https://cdn.discordapp.com/attachments/429849391164030988/928352748108406814/a7e8eb74b7.png) (Correction: image download only happens in main menu, not on every rank refresh) There is a setting to go back to the old system for those who need to see when their rank updates asap. Even tho I plan to remove rank updates, I'm still gonna fix this as best I can out of spite.
- **Autocompression for vanilla image-sequence maps**. If a map has at least 1 unique image for every second, the autocompresser will kick in. Most if not all Vanilla image-sequence maps get detected by this, and will use significantly less RAM/VRAM than vanilla would in exchange for much longer loading times. You can check the console during a long loading time to see if auto-compress triggered.
- **Storyboard and zoom animations are "less frame-dependent"**. This means that map animations (zooms, storyboards, etc.) should play very similarly on all modded clients, regardless of FPS. There is a slight, usually unnoticeable difference in animation-feel between modded and vanilla.
- **All mapping events use config v3 arc offset**. In Vanilla, arcs are delayed by 110ms + the users arc delay setting. In IQoL, all map events use that delay. This means mappers no longer need to offset storyboard/zoom events to match the arc offset. This does mean old maps that were built around the old mismatch are offset now.
- **Use any skin!** Set the skin you'd like in [`qolmod/skin.txt`](https://github.com/FlyingRabidUnicornPig/IntralismQoLMod/blob/main/qolmod/skin.txt). This is a visual change to the client-side only. Users in multiplayer lobbies will see your steam-equipped skin when spectating, your inventory still only shows skins you own through Steam, etc.

### MISC
- Downloaded **maps will display their difficulty** when hovered in map-select.
- Difficulty Adjustments:
  - **Zooms do not count towards diff calculation anymore.** Modded zooms/rotations are near-impossible to calculate with any sense of reliability. Fuck that!
  - **Events after MapEnd do not count toward diff calculation anymore.** No artificial inflation with unseen arcs.
- Added a **backup feature to saves**, in case things get fucked up.
- Press "O" while connecting to server to **Quickstart Offline Mode** (currently buggy)
- **Browse for non-tagged workshop maps** by selecting "NoTag" in the filter options (will ignore any other tags you've pressed)
- **New Settings** (feel free to [request](https://steamcommunity.com/id/DustDustInTheWind/) a personal QoL setting)
  - **"Gameplay"**
    - Enable Old Rank Refresh
    - Disable editor using the map name in Discord RPC (for Dust)
    - Enable the Editor Waveform
    - Open Event Editor on editor startup. (for EDM)
    - Open last edited map on editor startup.
  - **Video**
    - FPS Lock using Unity's shitty built-in fps capper (may fuck with map timing. could be fixed in future update)
- **Many vanilla bugs have been squashed** (a never ending feat)
  - 2 hand mode is no longer deep fried
  - The Map-Over screen is fixed
  - Main Menu Player Data now starts in a "loading" state.
- **And many new bugs have been added**
  - Mp3s now don't work *at all*.
  - More lag in some places.
  - A probable memory leak or two.
- **Several easter eggs**

### Bugs To Squash
- Mod Bug: **MP3s do not play** **Workaround:** use vanilla, where they also don't work :/ I actually have no clue how oxy actually got mp3s playing, this is a strangely unique scenario and I haven't been able to deobfuscate it yet. I will probably try to find a new solution instead of trying to understand the old solution. For now just use superior .ogg
- Mod Bug: Some maps stutter badly on map end (escape-quit only? something related to events needing to be processed, is this related to my anti-ear-rape fix?)
- Mod Bug: Map Over screen doesn't update values for new play (was this null spam shit intentional? Just figure out how to clear and reset it i guess)
- Mod Bug: Caret movement somewhat buggy(?)
- Mod Bug: BPM Grid tool doesn't seem to target newly created BPM Events
- Mod Bug: Map Preview can be unreasonably laggy. **Workaround:** Turn off map preview, srry.
- Mod Bug: Leaving the editor will take you to the map select on top of the main menu if you play tested. (related to vanilla map select bug) **No Workaround**
- Intentional Mod "Bug": The "Map" drop down menu flashes during loading and sometimes stays up afterwards. I'd rather this wasn't the case.
- Vanilla Bug: Map Selector Sometimes pops up on game startup. (related to playtest mod bug) **Workaround:** Close Intralism through the "Exit Button" instead of Alt+F4
- Vanilla Bug: Map Selector always goes to page 1 of the Editor tab when loading maps.
- Vanilla Bug: Highscore doesn't save the first time you play a new map. **Workaround:** Fail the map with a positive score then start again.
- Vanila Bug: Event Editor drop-down doesn't always position properly, sometimes not even appearing on screen. **Workaround:** Scroll to a new event, click Apply to refresh, and try not to leave the drop down open while playing the song.
- Partially fixed Vanilla Bug: Rank updating can cause stutter during gameplay (partially fixed with a 10 minute timer, stutters happen but only every 10 minutes instead of every time. i want to improve this further tho)

### "High Priority" TODO (this means nothing)
- Numkeys + modkey (shift/ctrl/alt) to change BPM snap
- Multi Track Support
- Rotate/Flip Selected arcs
- Stepped/Sliding BPM params
- Map Backup
- Negative Speed experiment
- Optimize search for closest event (would drastically improve performance of playback and scrolling, especially on *large* maps)
- Bug Fixes and Optimizations
- Endlessly updating the Readme
- Ignoring the High Priroity ToDo

### TO DO / Feature Wishlist (Feel free to [request](https://steamcommunity.com/id/DustDustInTheWind/) or [here](https://github.com/FlyingRabidUnicornPig/IntralismQoLMod/issues))
- "Initialize" event toggle for map/storyboard objects. Basically instead of spawning at 0,0,0, having to wait until time = 0 to trigger an event (maps start before 0), instead spawn at a user specified place, or start as soon as the map starts playing.
- Color palette for storyboard events
- CTRL+SHIFT+V to paste without snapping to grid
- Open map folder button in editor
- Easy way to change speed/tempo of map (for BPM messups or for people who want to easily convert a faster/slower ver of a map)
- Change the crosshair to a transparent version of your current view model, a 3D crosshair that matches the skin you're using and might properly represent the nonexistant "judgement line" at z0 compared to a fucking 2D image.
- Try fixing the broken skin textures
- Add custom skin loader
- Custom workshop tags
- Multi-storyboard-object spawner event (spawn x number of an object with a shared id (sun1, sun2, sun3, etc))
- Mirror-storyboard event (an event that handles multiple objects mirrored over a specified angle/other parameters)
- Custom Gamemode where you can set the speed before playing.
- SwitchHand event (go from 1hand to 2hand and vice versa)
- Disable clicking on progress bar when event editor is up (no more accidentally going to the end of map when I try to click Apply)
- Crop Sprite animated event
- Improve gameplay-to-song accuracy
  - Change arc spawner to use music time instead of Time.deltaTime (greatly improves map-to-song accuracy, can stutter-proof the spawn easily, but stutters could still fuck with arc movement on the way to the crosshair. Easiest to implement)
  - Change arc movement to adjust based on music time instead of a set speed (would mean near-perfect map-to-song accuracy, stutters could still fuck with input (arcs would move properly, but over one frame they can theoretically jump over the "100% accurate" range for the user to hit them on))
  - Change the input system for even more accurate gameplay (honestly the first two will be good enough for this trashfire of a game but this isn't off the table)
- Access the leaderboards of workshop maps (Workshop maps have empty leaderboards, but it is possible for modded users to access and submit scores to any workshop map)
- Change colors and sizes of events depending on type (imagine storyboard editing without a sea of green, starting/ending events being larger acting as bookmarks)
- Mousewheel to control volume during gameplay
- BPM Find tool (tap to the beat)
- Allow esc or quick retry button from Score Screen instead of forced to use mouse
- Autoplay Hack (Move arc-despawner to crosshair)
- Video Player for storyboard?
- Skip the beginning/ending of a map
- List the specific number of arcs, zooms, storyboard events, etc
- Add more editor themes
- Disable Zooms setting
- Keyboard shortcuts in main menu (one key press to open editor for example)
- Map Selector Optimizations & Improvements (caching, faster loading, show more maps, fix lag, etc.)
- Add better storyboard navigation/manipulation features (can use https://github.com/FlyingRabidUnicornPig/Intralism-Mapping-Assistant for reference)
- Pause on esc press
- Map shader control (there's a shit ton of shader effects in here that could be utilized by mappers for even finer control over map visuals)
- Skin change event (Control the skin the user uses for this map when storyboard is enabled)
