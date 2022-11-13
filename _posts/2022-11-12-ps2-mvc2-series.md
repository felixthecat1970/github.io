---
classes: wide
title: "PS2 Marvel vs. Capcom 2: New Age of Heroes full frame mode and PS2 > PS4 test build guide"
excerpt_separator: "<!--more-->"
categories:
  - Blog
  - PS2
tags:
  - PS2
---

Marvel vs. Capcom 2: New Age of Heroes is a crossover fighting game developed and published by Capcom published in arcades (naomi), dreamcast, ps2, ps3. xbox.

<!--more-->

<figure class="third">
<a href="/gamepatches-blog/assets/images/mvc2-jp.jpg"><img src="/gamepatches-blog/assets/images/mvc2-jp.jpg"></a>
<a href="/gamepatches-blog/assets/images/mvc2-eu.jpg"><img src="/gamepatches-blog/assets/images/mvc2-eu.jpg"></a>
<a href="/gamepatches-blog/assets/images/mvc2-us.jpg"><img src="/gamepatches-blog/assets/images/mvc2-us.jpg"></a>
	<figcaption>PS2 Original Game Covers</figcaption>
</figure>

More info Marvel vs Capcom 2 series: [Wikipedia](https://en.wikipedia.org/wiki/Marvel_vs._Capcom_2:_New_Age_of_Heroes) 
learn how to play it [Wiki Supercombo link](https://wiki.supercombo.gg/w/Marvel_vs_Capcom_2)

## Disclaimer:
This is my code finds, ideas, information, experiments, deduction in a empirical manner, nothing is granted to work perfect or is correct information about code reverse enginnering, for more tecnical approach i leave lectures in the end will help understand more, the next stories are related in a friendly, free, uncared manner for friends and people can someway understand. 

## CODE NOTES - STORIES:
learning more about GS deveplopment and implementation trying understand how the ps2 games pass parameters for the common "full frame mode" and "field renderer" modes and finding "partial" clues how is handled by ps2 so some couple months ago when have "freetime" debugging Mvc2 i find disabled some variables related to it (this game originaly was coded in field rendered mode 640x224) giving the low res blurry image frame common in this games when present frame in "field rendered mode" and giving bad reputation that time; after analizing the mips code to find exist a variable who call the full frame mode giving full frame mode 640x448 and disabling blurry image also can call the 640x480 (arcade specs) sadly missing other "unknow variables" so the image look moved to button or upper position, still 448 mode looks ok loss only 16px up 16px down but when progressive native mode is called match correctly screen given a horizontal match 3:2 progressive frame image (i think is correcly named); by the way i upload a test builds for run in PS4 (9.00 homebrew enabled consoles only) in HD mode visit my twitter for links.


## GAMES CODES:
Marvel vs. Capcom 2 - New Age of Heroes (Japan) SLPM_622.27;1) Game CRC = 0x5BC8C9E8 
Marvel vs. Capcom 2 - New Age of Heroes (USA) SLUS_204.86;1) Game CRC = 0x49209767 
Marvel vs. Capcom 2 - New Age of Heroes (Europe) SLES_511.74;1) Game CRC = 0xD14A6CD6 (updated) 

- +Enable Full Frame Mode 640x448 (instead common 640x224)
- +Autoboot - Enable Progressive Scan video mode (ps2 consoles need progressive scan tv setup - for composite setups search "composite" available in repository)
- +Interlacing is disabled in progressive mode and frame mode
- +PAL version (Des-Pal-lettized) remove selector and run always in progressive scan
- +PS4 link build guide (Run game in HD in PS4 9.00 firmware hombrew enabled consoles)
- +PS4 Build use L3 - R3 Change soft - sharp mode (negible changes)
- +ADD PCSX2 gamesettings profiles with recomended settings
!!! for better image in PCSX2 emulator disable Dithering option for sharper image and use 2x+=> scaling options

**Codes included in .zip download or direct search in github repository in next steps.

This codes enable best image mode support PCSX2-QT emulator and PS2/PS3/PS4 Consoles, keep in mind tested (PC / PS4) but unknow if works ok in longplays.

## HOW TO USE:

### METHOD 1 - DOWNLOAD CODE FILES FOR PC EMULATOR "PCSX2-QT":
[Click here and look for CODE > DOWNLOAD ZIP or search in folders](https://github.com/felixthecat1970/gamepatches)  
open downloaded .zip file, navigate to Playstation 2 folder, copy files and folders to your default PCX2-QT emulator or search repository the XXXXXXXXX.pnach files cheats-gameconfigs and copy folders in emulator
!!! Beware this will overwrite any custom cheats/gameconfigs you have previusly for the game in your PCSX2 folder. !!! 
Enable "Cheats" option in emulator and run your game.

### METHOD 2 - APPLY/PATCH DIRECTLY GAME DUMPS .BIN/CUE=CD or .ISO=DVD FOR PS2/PS3/PS4/PC  
use PS2 Patch Engine PC tool by pelvicthrustman 1.03 from here: [Link](https://www.psx-place.com/resources/ps2-patch-engine-by-pelvicthrustman.694/)  
1. open ps2_patch_engine tool in pc (windows only)
2. download .zip from method 1 or search individually in repository for XXXXXX.pnach file according your game version / region
3. load the xxxxx.iso or xxxxxx.bin game dump in ps2_patch_engine tool and select "PNACH" option
4. open XXXXXXX.pnach file with text editor (notepad, ++notepad or similar app), copy all "*patch=XXXXXX..etc*" code lines and paste in ps2_patch_engine (white window) and press "PATCH"
5. if you do all correctly the app will generate a " your-game-xxxxxx_pached.iso or .bin file, use this file for load in your console or build (PS4)

### METHOD 3 - RUN IN PS4 CONSOLES GUIDE
1. Check my twitter account for easy link build guide

### TESTED setups:
- PC: - RYZEN 3400G - VEGA 11 + PCSX2-QT-avx2 (working ok)
- PS3 SLIM (USA MODEL) - CFW evilnat 4.89 + webmanmod (UNTESTED)
- PS3 with PS2 hardware models CECHAxx · CECHBxx · CECHCxx · CECHExx (USA/JAPAN) 20gb/60gb only (UNTESTED)
- PS2 - (UNTESTED) *look How to play
- PS4 - (Tested PS4 pro 9.00 last to date goldhen working ok)

### RECOMENDED LECTURES THANKS TO:
- Title of article: Playstation 2 Architecture - A Practical Analysis
  - Author: Rodrigo Copetti
  - URL: [https://www.copetti.org/writings/consoles/playstation-2/](https://www.copetti.org/writings/consoles/playstation-2/)
  - Date of publication: April 8, 2020
  - Last modified: June 3, 2022
	
- DobieStation 
  - Read the post "**Sins of PS2**" in [https://www.patreon.com/dobiestation](https://www.patreon.com/dobiestation)

## FAQ:

### This codes is for ? 
Use in PC emulator PCSX2-QT, PS4 Homebrew enabled consoles (requires build), PS3 CONSOLES (hdmi-component 480p-720p-1080p setups only), PS2 CONSOLES (with component progressive tv setups) incompactible with interleaced signals setups like rf, rca white/red/yellow cables (look if game has "composite" codes folder for use in common interlaced signal setups).

### This can be used with original game disks ?
yes, but only in ps2 consoles and ps3 fat ps2 backward compactibility models like the 60gb-20gb USA/JAPAN and a method load cheats files format .pnach, i read PS2 OPL homebrew can load cheats but i have not tested yet more info [PS2 OPL HOMEBREW](https://github.com/ps2homebrew/Open-PS2-Loader) or gameshark alike devices (you need to convert codes which is hard); my recomended step is have your console homebrew enabled, dump your game in pc and patch it; for more tech oriented/seasoned people "how to dump correctly" [link](http://wiki.redump.org/index.php?title=Dumping_Guides) or try imgburn app in windows, brazero or similar app (linux); you can verify game dump in redump database [HERE](http://redump.org/discs/system/ps2/).

### not working for me PCSX2,PS2.PS3,PS4?
something you are doign wrong or using bad dumped image from your game, redump game or check hash integrity in [Redump.org](http://redump.org/discs/system/ps2/).
search correct tutorial each console look below in how to play in.. section

### not working with others emulators, forks, "put your emu name here" ______, android, other devices, etc ?
pcsx2 is a long standing mature emulator and only support this and hardware sony consoles, other emulators, devices etc ask in their respective forums chats etc for cheat load support, try patch image directly for run it if you have problems to load XXXXXXX.pnach files. 

### How to play in...
Recomended official developers - collaborators sites:
- PC: - Playstation 2 emulator PCSX2 [Official site pcsx2.net/](https://pcsx2.net/)
- PS3: - Enable homebrew [Official site ps3xploit.me](https://www.ps3xploit.me/) and [Official CFW Evilnat thread](https://www.psx-place.com/threads/4-89-evilnat-cfw-w-cobra-v8-3-cex-nobd-nobt-builds.37272/)
- PS2: - [Recomended guide for enable Hombrew](https://www.psx-place.com/threads/tutorial-the-great-ps2-aio-guide.30219/)
	- PS2 OPL homebrew [Official site](https://github.com/ps2homebrew/Open-PS2-Loader)
- PS4:
	- Need enabled homebrew console (posible in all ps4 models with firmware 1.00 > 9.00)
	- Need to create .PKG and install package use recomended tool by kozarovv [LINK](https://www.psx-place.com/threads/release-ps2-fpkg-0-6-by-jabu-new-tool-to-convert-ps2-games-for-ps4.30350/)