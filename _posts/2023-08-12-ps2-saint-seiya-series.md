---
classes: wide
title: "PS2 Saint Seiya Series 60fps + ntsc modes + language unlock"
excerpt_separator: "<!--more-->"
categories:
  - Blog
  - PS2
tags:
  - PS2
---

Playstation 2 custom codes for saint seiya game series for consoles and emulators.

<!--more-->

More Info about [Playstation 2](https://en.wikipedia.org/wiki/List_of_Saint_Seiya_video_games)
Recomeded lectures in end of post

<figure class="third">
<a href="/gamepatches-blog/assets/images/sss-jp.jpg"><img src="/gamepatches-blog/assets/images/sss-jp.jpg"></a>
<a href="/gamepatches-blog/assets/images/sss-eu.jpg"><img src="/gamepatches-blog/assets/images/sss-eu.jpg"></a>
<a href="/gamepatches-blog/assets/images/ssh-jp.jpg"><img src="/gamepatches-blog/assets/images/ssh-jp.jpg"></a>
<a href="/gamepatches-blog/assets/images/ssh-eu.jpg"><img src="/gamepatches-blog/assets/images/ssh-eu.jpg"></a>
	<figcaption>PS2 Original Game Covers</figcaption>
</figure>

Also check updates in my online code list Here i wil update codes witch enable this image modes in compactible games, in offcial games (not need for combo button or weird button combinations), and other surprises as PAL > NTSC native codes with correct sync audio - video (most cases) check list here (updated online when changes occur)

Open table [HERE](https://docs.google.com/spreadsheets/d/e/2PACX-1vQK9yHshfnqIwf66Xb0MIG_hJ44fhPuBByI7jE8-OGSC1M63CN-bPFUbwBu9AUpl9n1wlt3oqIxcgEC/pubhtml?gid=0&single=true)

## Disclaimer:
This is my code finds, ideas, information, experiments, deduction in a empirical manner, nothing is granted to work perfect or is correct information about code reverse enginnering, for more tecnical approach i leave lectures in the end will help understand more, the next stories are related in a friendly, free, uncared manner for friends and people can "someway" understand. 

## CODE NOTES - STORIES:
Hello, finally working and withow time, but for mental trainning in weekends i going to start cleaning a bunch codes i made couple months ago: saint seiya series on ps2 only released in japan and europe with their respective problems (japan only japanese) and europe (only in blurry PAL 50hz/25fps tv mode) so debugging i find the games has locked their video modes and languages so, with this codes you can play European version in NTSC tv mode and framerate unlocked ( 60fps) but for fortunate people has the japanese version you can play in 4 languages, yes the languages files are hidden (or maybe unfinished) the codes unlock the languages and convert your japanese copy in multilanguage game with japanese intro and music, like always use my tutorials.

Demo gameplay:
https://youtu.be/OTQWrellI9o

Codes:
+All in NTSC 60hz Video mode
+All with 60 fps unlock
+optional codes for Hades changed the framebufer config for less blurry image in emulators (disable if you have problems on original hardware or consoles)

Saint Seiya - The Sanctuary (Europe) (En,Ja,Fr,De,Es,It) sha1:919baf4e53ed2838181d1ee9de88be9ef51ee8e7
Saint Seiya - Sanctuary Juunikyuu-hen (Japan) sha1:f7009062d4a685a4adbd313fc7f79e1ad058652a

Saint Seiya - The Hades (Europe) (En,Ja,Fr,Es,It) sha1:6da748b0a966a884fc08b3d0d56ffb1bf51848c7
Saint Seiya - Meiou Hades Juunikyuu-hen (Japan) sha1:fdd7b2169f2bb687778d358a53609664f92694fd
+ Optional Convert (Japan) version hades to multilanguage
+ Optional Convert (Europe) version to japanese (intro still play genereic song for europe region)

For codes Check my github repo [here](https://github.com/felixthecat1970/gamepatches/tree/main/Playstation_2/Saint%20seiya%20(Series)/cheats] / or go to romhacking.net some days.

## HOW TO USE:

### METHOD 1 - DOWNLOAD CODE FILES FOR PC EMULATOR "PCSX2-QT":
1-Look game name you want
2-open .pnach with notepad app or use new .txt note editor and copy paste the code block lines (all)
3-save the file with this name format, use your game name CRC = 0x XXXXXXXX
in windows save as > filename.pnach and "save as type All files (*.*)" for correct extension.
example:
(Metal slug 3D (Japan) SLPS_256.50;1) Game CRC = 0x7D8D8BFA) the new file should be named " 7D8D8BFA.pnach " 
4-copy file to "cheats" folder in emulator and enable "cheats" option in PCSX2 emulator

### METHOD 2 - APPLY/PATCH DIRECTLY GAME DUMPS .BIN/CUE=CD or .ISO=DVD FOR PS2/PS3/PS4/PC  
use PS2 Patch Engine PC tool by pelvicthrustman 1.03 from here: [Link](https://www.psx-place.com/resources/ps2-patch-engine-by-pelvicthrustman.694/)  
1. open ps2_patch_engine tool in pc (windows only)
2. look in table/sheet the game according your game version / region
3. load the xxxxx.iso or xxxxxx.bin game dump in ps2_patch_engine tool and select "PNACH" option
4. copy codeblock copy all "*patch=XXXXXX..etc*" code lines and paste in ps2_patch_engine (white window) and press "PATCH"
5. if you do all correctly the app will generate a " your-game-xxxxxx_pached.iso or .bin file, use this file for load in your console PS2 or build for (PS3,PS4)

### TESTED setups:
- PC: - RYZEN 3400G - VEGA 11 + PCSX2-QT-avx2 (working ok)
- PS3 SLIM (USA MODEL) - CFW evilnat 4.89 + webmanmod (UNTESTED)
- PS3 with PS2 hardware models CECHAxx · CECHBxx · CECHCxx · CECHExx (USA/JAPAN) 20gb/60gb only (UNTESTED)
- PS2 - (UNTESTED) *look How to play end post
- PS4 - (UNTESTED *RECOMEDED PS4 / pro 9.00 HOMEBREW ENABLED, last to date goldhen working ok)

### RECOMENDED LECTURES THANKS TO:
- Title of article: Playstation 2 Architecture - A Practical Analysis
  - Author: Rodrigo Copetti
  - URL: [https://www.copetti.org/writings/consoles/playstation-2/](https://www.copetti.org/writings/consoles/playstation-2/)
  - Date of publication: April 8, 2020
  - Last modified: June 3, 2022
	
- DobieStation 
  - Read the post "**Sins of PS2**" in [https://www.patreon.com/dobiestation](https://www.patreon.com/dobiestation)

## FAQ:
### How to setup my console for better image ?
check RetroRGB best source guides, cables, setups for retro playing https://www.retrorgb.com/

### This codes is for ? 
Use in PC emulator PCSX2-QT, PS4 Homebrew enabled consoles (requires build custom package), PS3 'BC' CONSOLES (hdmi-component 480p-720p-1080p setups only), PS2 CONSOLES (with component progressive tv setups) some codes are incompactible with interleaced signals(the progressive scan ones) setups like rf, rca white/red/yellow cables (look if game has "composite" codes folder for use in common interlaced signal setups).

### This can be used with original game disks ?
yes, but only in ps2 consoles and ps3 fat ps2 backward compactibility models like the 60gb-20gb USA/JAPAN and a method load cheats files format .pnach, i read PS2 OPL homebrew can load cheats but i have not tested yet more info [PS2 OPL HOMEBREW](https://github.com/ps2homebrew/Open-PS2-Loader) or gameshark alike devices (you need to convert codes which is hard); my recomended step is have your console homebrew enabled, dump your game in pc and patch it; for more tech oriented/seasoned people "how to dump correctly" [link](http://wiki.redump.org/index.php?title=Dumping_Guides) or try imgburn app in windows, brazero or similar app (linux); you can verify game dump in redump database [HERE](http://redump.org/discs/system/ps2/).

### not working for me PCSX2,PS2.PS3,PS4?
something you are doign something wrong or using bad dumped image from your game, redump game or check hash integrity in [Redump.org](http://redump.org/discs/system/ps2/) using 7zip https://www.7-zip.org/download.html opensource file compresor sha1 check. search correct tutorial each console look below in how to play in.. section

### not working with others emulators, forks "put your emu name here______, android, other devices ?
pcsx2 is a long standing mature emulator and i only support this and hardware sony consoles, other emulators ask in their respective forums chats etc for cheat load support, try patch image directly for run it if you have problems to load .pnach files. 

### some codes has fps unlock, 60 fps etc it will work on my console (put the name here) _________?
unlocking framerate codes is recomended for pc-emualtors setups because it will require more cpu power (like modern pc) keep in mind consoles are very limited in hardware processing power maybe codes dont work, work worse and can add heat your console, so, like always, the use this codes is your responsibility not mine, and i not responsible for (heated or burned consoles) if you are not sure not use this codes.


### How to play in...
Recomended official developers - collaborators sites:
- PC: - Playstation 2 emulator PCSX2 [Official site pcsx2.net/](https://pcsx2.net/)
- PS3: - Enable homebrew [Official site ps3xploit.me](https://www.ps3xploit.me/) ***updated link 2023 and [Official CFW Evilnat thread](https://www.psx-place.com/threads/4-89-evilnat-cfw-w-cobra-v8-3-cex-nobd-nobt-builds.37272/)
- PS2: - [Recomended guide for enable Hombrew](https://www.psx-place.com/threads/tutorial-the-great-ps2-aio-guide.30219/)
	- PS2 OPL homebrew [Official site](https://github.com/ps2homebrew/Open-PS2-Loader)
- PS4:
	- Need enabled homebrew console (posible in all ps4 models with firmware 1.00 > 9.00)
	- Need to create .PKG and install package use recomended tool by kozarovv [LINK](https://www.psx-place.com/threads/release-ps2-fpkg-0-6-by-jabu-new-tool-to-convert-ps2-games-for-ps4.30350/)