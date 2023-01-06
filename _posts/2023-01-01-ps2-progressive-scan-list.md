---
classes: wide
title: "PS2 Progressive scan custom code list online"
excerpt_separator: "<!--more-->"
categories:
  - Blog
  - PS2
tags:
  - PS2
---

Playstation 2 custom codes list wich enable progressive scan TV mode for NTSC / PAL for consoles and emulators.

<!--more-->

More Info about [Playstation 2](https://en.wikipedia.org/wiki/PlayStation_2)
Recomeded lectures in end of post

<figure class="third">
<a href="https://upload.wikimedia.org/wikipedia/commons/1/1c/PS2-Versions.jpg"><img src="https://upload.wikimedia.org/wikipedia/commons/1/1c/PS2-Versions.jpg"></a>
	<figcaption>PS2 Cosole Models</figcaption>
</figure>

Custom Code list for enable progressive scan tv modes in NTSC / PAL games or PAL > NTSC with correct screen size and speed logic, also official compactible games (not need for selector options in game, combo button or weird combo button combinations, GSM or similar hdtv hombrew apps); codes enable autobooting Progressive scan tv mode or NTSC (in some PAL only games).

Open List (updated realtime) [HERE](https://docs.google.com/spreadsheets/d/e/2PACX-1vQK9yHshfnqIwf66Xb0MIG_hJ44fhPuBByI7jE8-OGSC1M63CN-bPFUbwBu9AUpl9n1wlt3oqIxcgEC/pubhtml?gid=0&single=true)

## Disclaimer:
This is my code finds, ideas, information, experiments, deduction in a empirical manner, nothing is granted to work perfect or is correct information about code reverse enginnering, for more tecnical approach i leave lectures in the end will help understand more, the next stories are related in a friendly, free, uncared manner for friends and people can "someway" understand. 

## CODE NOTES - STORIES:
Happy new year; now 2023 a little busy with (temporal job) so no time for debug codes freely; a couple weeks thinking how to optimize time for publish more codes i decide to post a sheet table can make changes or updates online anywhere and keep easy record anywhere, mainly i will take efforts to "progressive scan type" codes the ps2 support many image output NTSC, PAL, PROGRESSIVE SCAN, vga, 720p, 1080i (hd formats works but it will crash due limited vram) so the best format was"progressive scan"; a novelty in the ps2 era showing better quality image with required setup (mainly a crt tv with progressive scan support and component cables the green-blue-yellow-white-red ones) here a basic comparation between formats:

For american / Japan releases this was the standard:
NTSC: 59.9hz, 29.9/59.9 fps, image frame buffer 640x448 / 512x448 or field render 640x224 / 512x224  ***Recomended in GS sony manual, others resolutions or refresh rates available

For European releases this was the standard
PAL: 50hz 25fps/50fps, image frame buffer 640x512 512x512 (vertical stretch from 448) or field render 640x256 / 512x256 ***Second recomended others resolutions or refresh rates available

Mainly feature in USA - JAPAN releases in selected titles, in europe game releases this was removed or disabled in game code.
PROGRESSIVE SCAN DTV: 59.94mhz 29.9/59.9 fps 640X480 - 640X448 (Internal) 720X480 output

you see PAL releases downgrade to 25fps or 50fps witch is bad for games need 60fps -devil may cry / action games, shooters, figthing games (timings), arcade type etc some can argue PAL releases looks better because the image display in 640x512 but here the news debugging games like death by degreess, ace combat series, others the PAL mode vertical x512 is strech from backbuffer x448 native image so degrade image futher (in crt looks fine) but in modern tv / monitors looks more blurry - degraded giving the bad "PAL" curse.  

remember progressive scan can be used officialy in selected titles this feature need to be called mostly with combo button triangle+cross in boot or menu selection, or weird combinations etc easily to forget; debuggin many games i find many registers functions has this modes disable, partially created, in compactible games, also some games have full frame mode implemented in executable but disabled (marvel vs capcom 2, capcom vs snk, valken, couple other suprises) using the filed render mode (for performance reasons, afraid from game fail, proyect times etc) giving the "worst port" title to many multiplatform games long time ago to many; enablinbg dtv mode give better clarity in image because disable some postprocess like a "blurry" image output,  other unlock fps etc, progressive scan mode codes has improvements and bugs too or some performance hit (consoles).

also other advantages is progressive call "full frame mode" instead of "field render mode" for explain in easy manner this mode send final frame in vertical reduced image example: 512x224 to screen firts scan out and the other half 512x224 in next scan out for performance reasons commonly using interlaced feature of CRT tv (that time globally crt tv was all interlaced signal) but now in monitors or hd tv this will look bad (news tv monitors no need interlacing and is handled poorly this legacy image technique).

Some people can be wondering but "GSM homebrew, HDTV loaders, Chips, similar" etc do de same what is the diference with this? like i expained in this example post [Here](https://felixthecat1970.github.io/gamepatches-blog/blog/ps2/post-ps2-sb-hk/) gsm, homebrew or similar hack the main function "sce main functions" related to video with a custom developed build code for "call desired tv mode values" detailed in Sony GS development manual, the thing is not always games works as desired, behave weird, have bugs or not compactible this because games are deveploped diferently each one, debugging mips game code i see some games call other "custom" values, use custom routines, bypass general sony guidelines, overwrite defined values, use "programing" tricks bypassing recomended sony guidelines etc; so this codes is another alternate aproach, debugging game executable i see many games have this tv modes disabled, partially coded or need to be called by main custom functions, so enabling will call the parameters same way like was designed calling correct functuions, routines for correct mode display and speed logic; i guessing this modes was not enabled because need more test, debug, bugs, for tight timelines, was a novelty that time so no risk whole proyect with times, sues, support warranties etc.. etc; keep in mind codes was tested couple hours and works ok (pc or some consoles) but in long play can have bugs so no warranty either. 
still need to correct more info about it so i leave this notes in updating......

## HOW TO USE:

### METHOD 1 - DOWNLOAD CODE FILES FOR PC EMULATOR "PCSX2-QT":
1. Look game name you want
2. open new .txt note editor and copy paste the code block lines (all) 
3. save the file with this format look game name CRC = 0x XXXXXXXX 
in windows save as > filename.pnach and "save as type All files (*.*)" for correct extension. 
example: 
(Metal slug 3D (Japan) SLPS_256.50;1) Game CRC = 0x7D8D8BFA) the new file should be named " 7D8D8BFA.pnach "  
4. copy file to "cheats" folder in emulator and enable "cheats" option in PCSX2 emulator 

### METHOD 2 - APPLY/PATCH DIRECTLY GAME DUMPS .BIN/CUE=CD or .ISO=DVD FOR PS2/PS3/PS4/PC  
use PS2 Patch Engine PC tool by pelvicthrustman 1.03 from here: [Link](https://www.psx-place.com/resources/ps2-patch-engine-by-pelvicthrustman.694/)  
1. open ps2_patch_engine tool in pc (windows only)
2. look in table/sheet the game according your game version / region
3. load the xxxxx.iso or xxxxxx.bin game dump in ps2_patch_engine tool and select "PNACH" option
4. copy codeblock copy all "*patch=XXXXXX..etc*" code lines and paste in ps2_patch_engine (white window) and press "PATCH"
5. if you do all correctly the app will generate a " your-game-xxxxxx_pached.iso or .bin file, use this file for load in your console PS2 or build (PS3,PS4)
!!! This will change your game dump CRC keep in mind if you use patched dumps and other cheats (crc name will not match in this scenario need to be changed)!!! 

### TESTED setups:
- PC: - RYZEN 3400G - VEGA 11 + PCSX2-QT-avx2 (working ok)
- PS3 SLIM (USA MODEL) - CFW evilnat 4.89 + webmanmod (UNTESTED)
- PS3 with PS2 hardware models CECHAxx · CECHBxx · CECHCxx · CECHExx (USA/JAPAN) 20gb/60gb only (UNTESTED)
- PS2 - (UNTESTED) *look How to play end post
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
### GSM HDTV etc homebrew do the same what is the diference? 
read my code notes stories section i explain there.

### How to setup my console for better image ? 
check [RetroRGB.com](https://www.retrorgb.com/) best source guides, cables, setups for retro playing.

### This codes is for ? 
Use in PC emulator PCSX2-QT, PS4 Homebrew enabled consoles, PS3 CONSOLES (hdmi-component 480p-720p-1080p setups only), PS2 CONSOLES (with component progressive tv setups) incompactible with interleaced signals setups like rf, rca white/red/yellow cables (look if game has "composite" codes folder for use in common interlaced signal setups).

### This can be used with original game disks ?
yes, but only in ps2 consoles and ps3 fat ps2 backward compactibility models like the 60gb-20gb USA/JAPAN and a "method" load cheats files in .pnach format, i read PS2 OPL homebrew can convert and load cheats but i have not tested yet more info [PS2 OPL HOMEBREW](https://github.com/ps2homebrew/Open-PS2-Loader); gameshark alike devices (you need to convert codes which is hard); my recomended steep is have your console homebrew enabled, dump your game in pc and patch it; for more tech oriented/seasoned people "how to dump correctly" [link](http://wiki.redump.org/index.php?title=Dumping_Guides) or try easy dump image .iso or .bin with imgburn app (windows), brazero or similar app (linux); you can verify game dump with redump database [HERE](http://redump.org/discs/system/ps2/).

### not working for me PCSX2,PS2.PS3,PS4?
something you are doign something wrong, not reading instructions correctly or using bad dumped image from your game, redump game or check hash sha-1 integrity compare database in [Redump.org](http://redump.org/discs/system/ps2/) using [7zip](https://www.7-zip.org/download.html) opensource file compresor using CRC sha1 check. search correct tutorial each console look below in how to play in.. section

### not working with others emulators, forks "put your emu name here______," android, other devices ?
pcsx2 is a long standing mature emulator and i only support this and hardware sony consoles, other emulators ask in their respective forums chats etc for cheat load support, also try patch image directly if you have problems to load .pnach files. 

### How to play in...
Recomended official developers - collaborators sites:
- PC: - Playstation 2 emulator PCSX2 [Official site pcsx2.net/](https://pcsx2.net/)
- PS3: - Enable homebrew [Official site ps3xploit.me](https://www.ps3xploit.me/) ***updated link 2023 and [Official CFW Evilnat thread](https://www.psx-place.com/threads/4-89-evilnat-cfw-w-cobra-v8-3-cex-nobd-nobt-builds.37272/)
- PS2: - [Recomended guide for enable Hombrew](https://www.psx-place.com/threads/tutorial-the-great-ps2-aio-guide.30219/)
	- PS2 OPL homebrew [Official site](https://github.com/ps2homebrew/Open-PS2-Loader)
- PS4:
	- Need enabled homebrew console (posible in all ps4 models with firmware 1.00 > 9.00)
	- Need to create install package use recomended tool by kozarovv [LINK](https://www.psx-place.com/threads/release-ps2-fpkg-0-6-by-jabu-new-tool-to-convert-ps2-games-for-ps4.30350/)