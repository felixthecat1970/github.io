---
classes: wide
title: "PS2 Native 640x480p modes for Sengoku Basara an Hokuto no Ken"
excerpt_separator: "<!--more-->"
categories:
  - Blog
  - PS2
tags:
  - PS2
---

Hokuto no Ken 北斗の拳 審判の双蒼星 拳豪列伝 and Sengoku BASARA X (戦国BASARA X) for playstation 2 console, only released in Japan, here you will find codes for enable 480p native sdtv mode and extended internal resolution to 640x480, some lecture stories and recomended profiles for easy play in PC emualtor PCX2-QT.

<!--more-->

<figure class="half">
<a href="/gamepatches-blog/assets/images/sb-jp.jpg"><img src="/assets/images/sb-jp.jpg"></a>
<a href="/gamepatches-blog/assets/images/hk-jp.jpg"><img src="/assets/images/hk-jp.jpg"></a>
	<figcaption>look below images.</figcaption>
</figure>

<!--Hokuto no Ken 北斗の拳 審判の双蒼星 拳豪列伝  (Japan)  |  Sengoku BASARA X (戦国BASARA X) (Japan)
:-------------------------:|:-------------------------:
![JAP](/gamepatches-blog/assets/images/hk-jp.jpg)  |  ![JAP](/gamepatches-blog/assets/images/sb-jp.jpg)-->

More info Hokuto no ken (Fist of the north star) game: [Wikipedia](https://en.wikipedia.org/wiki/Fist_of_the_North_Star_(2005_video_game)) also [Learn how to play it](https://wiki.supercombo.gg/w/Hokuto_no_Ken)   
More info Sengoku Basara X game: [Wikia](https://sengokubasara.fandom.com/wiki/Sengoku_BASARA_X) also [learn how to play it](https://wiki.supercombo.gg/w/Sengoku_Basara_X)

## Disclaimer:
This is my findings, ideas, codes, information, experiments, deduction in a empirical manner, nothing is granted to work perfect or is correct information about code reverse enginnering, for more tecnical approach i leave lectures in the end who help understand more, the next stories are related in a friendly, free, uncared manner for friends and people can someway understand. 

## CODE NOTES - STORIES:
looking in pcsx2 debugger a bunch of numbers, letters combined program language named "MIPS" which is cpu architecture for ps2 cpu, for improve a peculiar common standard ps2 games resolutions in games was:   640x468 ntsc   512x468 ntsc   512x512 pal   512x456 pal   --pixels-lines resolutions (ps2 games also has anothers weird pixels/lines resolutions and infamous 240p but this is for other post) anyway looking on ps2 docs GS (graphics synthetizer) others i see the support for vga 640x480p/i VESA modes (common resolution for many games) and looking internal resolutions for games has native progressive modes wich enables 640x480p pixels/lines in games with 640x468 ntsc, also in my "witch hunt" for disable the "interleace" implementation 2necessary for crt tv from that time (talk reserved for anothor post) i see this is also disabled natively when 480p tv mode "sdtv" is enabled so the solution is enable 480p but here the news if you are reading this display mode is not implemented in all games officialy  only limted list you can check here, ok then you read, used etc in web exist tools, disk for enable this sdtv modes working "ok" but some problems mainly videos crash/no display or wrong image positions, also other forums exist better solution like GSM tool and implementation / update of GSM in PS2OPL Loader wich works ok but same some tittles have video crash or wwrong image positions, also direct hacks in code like this witch enables more direct 480p modes still keep me wondering what if.... (yes marvel , good animation) this modes are natively implemented but disabled in game code, because seasoned programers who create programs old times, apps etc in pc workstations in his max tecnology but when the boos, project manager wharever now (marketing... marketing?) tell you or remind you core principles of "better stable product that experimental" and "broadban public to reach safely" sdtv was a novelty that time and is better safe that sorry.... (appart now understant old friend socrates not write almost any because "feel free in the heat of the words.." kudos to book writers) so many this things are leaving dornmant/disabled in..code and start the game adaptation to consumers crt tv (or image "downgrade" like i name),  (ok for people look more tecnicall reading would be later sorry --still organizing ideas explanations etc); here the results thanks to lectures in sony ps2 GS documents, GSM source code and anothers lectures (look end of post) and learning more "basics" in mips i find common functions who let me to find this native sdtv codes in this games and another srurise the correct native modes in 640x480 pixels instead 640x448 ntsc

<figure class="half">
<a href="/gamepatches-blog/assets/images/hk-pic2.png"><img src="/assets/images/hk-pic2.png"></a>
<a href="/gamepatches-blog/assets/images/hk-p-pic1.png"><img src="/assets/images/hk-p-pic1.png"></a>
	<figcaption>look below images.</figcaption>
</figure>

About sengoku basara \ hokuto no ken game really not need a interleaced - 480p mode code because they are presented in mode named "full frame mode (still learning how to name properly)" means each frame-image is presented in each interval scan in tv/monitor full resolution so image look pretty and interleaced implementation runs ok (the jumping image up-down effect for crt tvs visible in sdtv or monitors but is explanation for other day), so lets find something anyway, some weeks ago find main code for sdtv but strange sengoku basara animated video opening crash, logs and console looks ok, after hours of debugging find culprit and fixed,  some days ago new fix change in PCSX2 source code corrects values in GSM area and video start crashing again so wrong fix asumtion, lets debug again ... trying other method is analize the video files and was rigth video is in interleaced mode ...maybe is this the problem, lucky video file format was in mpeg not need to recoding for change in progressive mode...rebuid image, testing and.... wrong video still crash .. looking other video type files other games also has video in interleave mode but running in progressive when mode is enabled (..or was i dreaming..) tired test need to resting too much numbers and letters, retaking next day code hunting finally after some hours of analize code find the correct code (i hope in future), the good part this  confirm assuptions about others functions handles video and possible correction for common video crash in sdtv modes when test other titles video crash bug when progressive is enabled still this need further testing; also the main bonus thing was the games run in native 640x480 pixels and have more area displayed (recover 34 view vertical pixels area ;) ) like other test codes i made last year ..so 480p native can be the way... maybe ... but lets see example area regained :

<figure class="half">
<a href="/gamepatches-blog/assets/images/sb-pic-2.png"><img src="/assets/images/sb-pic-2.png"></a>
<a href="/gamepatches-blog/assets/images/sb-p-pic1.png"><img src="/assets/images/sb-p-pic1.png"></a>
	<figcaption>look below images.</figcaption>
</figure>

Now some people can be thinking "but this codes or progressive scan mods codes, HDTV PRO bundle (or similar) GSM tool or PS2 OPL can do it what is the diference..?"  let me explain:
GSM or OPL relies a tecnique "custom made code" which stop\hook main know function - call process PS2 tv signals and rebuild according the program code using offside mips code in ps2 ram executable area then passes new modes values to function continue processing it with new data (gameshark other tools do same thing for other uses) this custom code is created by talented people like PS2 OPL GSM using sony documentation, reasonings wharever information they can find, made and other unknow methods for fix or make compactible mayority of games, but cach is programers not always build or program in same manner beacuse ... (happen now remember the "beacause" mispelling error in final fantasy vii usa version ..was a broken keyboard like mine?... funny.. lets continue) because ps2 is not stric how you implement your program, it means programers can implement trics, workarounds, unknow methods, offside common recomendations methods of sony development documents and that was a novelty, was a good thing or hell for programers or combine all that time, this lets you be more creative withow much restriction implementing things, solutions, new graphics solutions custom code programs running in parallel, leading to great games catalog who many people remenber or almost have broken game code too (check lectures in the end for more information) and this part keep me thinking about discussion many people for console / fanboy wars "dreamcast was better, ps2 was better xbox...etc" my opinion consoles is a canvas, programers are artist the game is the art depend how you see, memories bring you, and capacity as programer you have to implement it and show off in each one or cry long hours of job; but lets continue, seeing the game code not always tv modes are passed exactly to common functions parameters like documentation says, programers implement many tecniques unique that no using default parameters, for performance, new graphics and many things you will never know (or you know if was programmer for ps2 games) unlock this changes, withow know activating or enabling this sdtv modes can lead to bugs, image problems, posible crashing etc, "like the crashing video" bugs.

Now you can be thinking "so this codes or method hack is better that X or Y...rigth ?" i not say that manner but lets say is another aproach to great job of GSM and OPL PS2 team which i learn from source code, the codes i find, made or hack, apply in game executable registers - function natively (calls-functions leave disabled by the programers) and let game executable do the magic as was used by worksations, developed etc (or the possibility game crash long way and that was other "unknow" reason function was disabled in game) however this code making comes with great cach i not have the game source code, development worsktations, and still learning, and this need to be implemented in each game so no tool automatically do all (forget dreaming or asking in emulator forums "please implement progressive mode options i read... here"), code hunthing take many hours and testing some games has this functions partial enabled or developed which is hard (and fun like re.enable sdtv mode code for ace combat i did) others need fixes and other not have it all so you need to build from zero that would be better using PS2 OPL GSM option and other simply reason is not possible at all.

another question possible arise is "but ps2 can do 720p 1080i like valkyrie profile (japan) and granturismo 4 is not better use this HDTV modes?" and my answer, is possible, ps2 GS documents explain have support for this HDTV formats and VESA (vga) modes but logic in this is "game developers not risk using novelty formats for time wich secure a game breaking bugs" also keep in mind ps2 video memory is little filling with this kind of big frame sizes will lead no memory so fast you will have nice wallpaper game slideshow, but how programmers to this 1080i modes in this specific games?, remember the "tricks, workarounds you can implement in ps2 part" this 1080i modes are really a trick, a example when a was code hunting valkyrie profile 2 in usa version i find call-register enable the infamous 1080i mode from japan version, enable the mode test and works in usa version but checking how frames are called from frame back buffer i see 480p mode in really looks better that 1080i now this 1080i relies in "interleacing mode" (yes interleacing is not always bad) the back buffer native frame is squised in a strange resolution a presented in half image in interval scan other half in next interval wich reducing memory filling and can be presented in good framerate but add lot off blurring jumps up/down deffects (still learning how to explain this, no take like seriusly tecnicall explain) i will try explain better when my stories about valkirie code hunting comes.

Hokuto no ken has a interesting thing is the english language available in game executable but disabled, still i have not yet unlock it or unknow if is possible but i will see the game other day if let magic "code" happen.

In the end keep mind this codes are not perfect or maybe can have better code call function - register in future (special cases for tekken 5 japan/usa/pal version wich would be my stories); also the possiblity game crash long run (still testing now, so consider a beta releases), PS2 OPL GSM updates are the best solution till now if you are test 480p and not like to wait (links end of article) or wait i will publishing my code findings in this blog.

## GAMES CODES:
### Sengoku Basara X (戦国BASARA X) (Japan) SLES_532.33;1) Game CRC = 0x1E177BBC
- +Autoboot - Enable Native Progressive Scan video mode (call-function)
- +No interleacing (of course sdtv mode call disable it)
- +640x480 pixels-lines enabled (instead default 640x448) more viewable area, also Integer scaling (still untested)
- *recomended disable pcsx2 > graphics > shader "texture filtering display" for more pixel art image (more clean image)
- *recomended auto-profiles file for PCSX2-QT included in download

```
gametitle=Sengoku Basara X (Japan) SLPM_550.08;1) Game CRC = 0x721DEBE4
comment=480p native sdtv mode unlock + extend resolution 640x480 v3 by felixthecat1970

//480p + 640x480 res. v3 !!!disable antialias option in game menu for 640x480!!!
patch=0,EE,201004E4,extended,A2620016
patch=0,EE,0010CF00,extended,24040000

```

### Hokuto no Ken - Shinpan no Sousousei - Kengou Retsuden 北斗の拳 審判の双蒼星 拳豪列伝 (Japan) SLPM_666.60;1) Game CRC = 0x9E8F0454
- +Autoboot - Enable Native Progressive Scan video mode (call-function)
- +No interleacing (of course sdtv mode call disable it)
- +640x480 pixels-lines enabled (instead default 640x448) more viewable area, also Integer scaling (still untested)
- *recomended disable pcsx2 > graphics > shader "texture filtering display" for more pixel art image (more clean image)
- *recomended auto-profiles file for PCSX2-QT included in download
 
```
gametitle=Hokuto no Ken Shinpan no Sousousei Kengou Retsuden (Japan) SLPM_666.60;1) Game CRC = 0x9E8F0454
comment=Native 480p sdtv mode + extend 640x480 v2 by felixthecat1970

//enable native 480p mode 640x480 !!!disable antialias option in game menu for 640x480!!!
patch=0,EE,20292720,extended,A38286E8

```

This codes enable best image mode support for PCSX2-QT emulator and PS2/PS3/PS4 Consoles, also you can test the correct pixel aspect ratios for "Integer Scaling" 2d (in pc emulation use/test 4:3 display - integer scaling - screen offset settings) learn more about integer scaling [HERE](https://tanalin.com/en/articles/integer-scaling/)

## HOW TO USE:
### METHOD 1 - DOWNLOAD CODE FILES FOR PC EMULATOR "PCSX2-QT":
[Click here and look for CODE > DOWNLOAD ZIP](https://github.com/felixthecat1970/gamepatches)  
open downloaded file, navigate to Playstation 2 foler, copy files and folders from "Assault Suits Valken (Japan) (Europe)" to your default PCX2-QT emulator  
!!! this will overwrite any custom cheats/gameconfigs for the game in your PCSX2 folder. !!!  
also you can download .pnach files directly from PCSX2 forums post [HERE] pending update <!---(https://forums.pcsx2.net/Thread-No-interlacing-codes?pid=627161#pid627161) -->

### METHOD 2 - APPLY/PATCH DIRECTLY GAME DUMPS .BIN/CUE=CD or .ISO=DVD FOR PS2/PS3/PS4/PC  
Look readme post in [RomHacking.com] *pending update* <!--- (https://www.romhacking.net/hacks/6891/) -->
Or use PS2 Patch Engine PC tool by pelvicthrustman 1.03 from here: [Link](https://www.psx-place.com/resources/ps2-patch-engine-by-pelvicthrustman.694/)  
1. download/view "patch" lines codes from method 1 according your game version
2. if using download open .pnach codes with text editor, copy "*patch*" code lines according game region "look method 1 CRC=XXXXXXX for know region .pnach file match" and patch you game dump. (in PAL version, patch to SLES_532.33 when dialog appear).

### TESTED setups:
- PC: - RYZEN 3400G WITH INTEGRATED GPU VEGA 11 + PCSX2-QT-avx2 
- PS3 SLIM (USA MODEL) - CFW evilnat 4.88 + webmanmod *Both games had bad compactibility w/o codes, Run slow in this models.
- PS3 Backwards ps2 hardware compactible (UNTESTED) *but should work ok
- PS2 - (UNTESTED) *look How to play
- PS4 - (UNTESTED) *look How to play

## FAQ:
### This codes is for ?
Use in PC emulator PCSX2-QT, PS3 CONSOLES (hdmi-component 480p-720p-1080p setups only), PS2 CONSOLES (with component progressive tv setups) incompactible with interleaced signals setups like rf, rca white/red/yellow cables.

### This can be used with original game disks ?
yes, but only in ps2 consoles and ps3 fat ps2 backward compactibility models like the 60gb-20gb USA/JAPAN and a method load cheats files format .pnach, i hear PS2 OPL homebrew can load cheats but i have not tested yet more info [PS2 OPL HOMEBREW](https://github.com/ps2homebrew/Open-PS2-Loader) or gameshark alike devices (you need to convert codes which is hard); my recomended step is have your console homebrew enabled, dump your game in pc and patch it; for more tech oriented/seasoned people "how to dump correctly" [link](http://wiki.redump.org/index.php?title=Dumping_Guides) or try imgburn app in windows, brazero or similar app (linux); you can verify game dump in redump database [HERE](http://redump.org/discs/system/ps2/).

### RECOMENDED LECTURES THANKS TO:
- Title of article: Playstation 2 Architecture - A Practical Analysis
  - Author: Rodrigo Copetti
  - URL: https://www.copetti.org/writings/consoles/playstation-2/
  - Date of publication: April 8, 2020
  - Last modified: June 3, 2022
	
- DobieStation 
  - Read the post "Sins of PS2" in https://www.patreon.com/dobiestation

### How to play in...
Recomended official developers - collaborators sites:
- PC: - Playstation 2 emulator PCSX2 [Official site pcsx2.net/](https://pcsx2.net/)
- PS3: - Enable homebrew [Official site ps3xploit.com](http://ps3xploit.com/) and [Official CFW Evilnat thread](https://www.psx-place.com/threads/4-89-evilnat-cfw-w-cobra-v8-3-cex-nobd-nobt-builds.37272/)
- PS2: - [Recomended guide for enable Hombrew](https://www.psx-place.com/threads/tutorial-the-great-ps2-aio-guide.30219/)
    - PS2 OPL homebrew [Official site](https://github.com/ps2homebrew/Open-PS2-Loader)
- PS4:
    - Need enabled homebrew console (posible in all ps4 models with firmware 1-00 - 9.00)
    - Need to create .PKG and install package use recomended tool by kozarovv [LINK](https://www.psx-place.com/threads/release-ps2-fpkg-0-6-by-jabu-new-tool-to-convert-ps2-games-for-ps4.30350/)
    - For lastest news releases config parameters required for ps2 in ps4 emulation look here [LINK](https://www.psx-place.com/threads/research-ps2-emulator-configuration-on-ps4.16131/)
