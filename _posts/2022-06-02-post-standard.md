---
classes: wide
title: "lets start with PS2 Assault Suits Valken Game Enhacements"
excerpt_separator: "<!--more-->"
categories:
  - Blog
  - PS2
tags:
  - PS2
---

Assault Suits Valken and (重装機兵ヴァルケン) for playstation 2 console, only released in Japan and Europe, here you will find codes for disable the interleaced function, disable PAL MODES, enable native 480p progressive scan display mode and recomended profiles for easy play in PC emualtor PCX2-QT.

More info about game: [Wikipedia](https://en.wikipedia.org/wiki/Assault_Suits_Valken)

<!--more-->

![FELIXTHECAT](/gamepatches-blog/assets/images/felixthecat.png)

## Before start ....
Almost 2+ years withow Job and looking something to keep me thinking i decide to organize my old reverse enginnering codes of games i did last years and some i published in PCSX2 forums last year, returning after a year looking now thread and new advances in PCSX2 pc emulator, the people are active with new codes, hacks etc, and me lurking there to post something (also i have to train my mind because boredom and no stable jobs are killing me) happen to find about github code pages proyects etc, so i decided to organize buch of left over codes proyects etc update and put in easy platform where people and friends can use it.

Assault Suits Valken (Europe)  |     重装機兵ヴァルケン (Japan)
:-----------------------------:|:-----------------------------:
![EU](/gamepatches-blog/assets/images/asv-eu.jpg)  |  ![JAP](/gamepatches-blog/assets/images/asv-jp.jpg)

## CODE NOTES - STORIES:
Looking last year for improve games i find has debug symbols (the japanese version), so learning more and find interesting codes like sharp buffer address and interleacing functions but still no like it, after year and past weeks re-learning more how to interact with functions, mips registers etc, i find pattern the programers leave disabled or half enabled functions like progressive scan function, ree-nable the function and native 480p mode is enabled wich also disable natively the interleacing function (a thing was required to old crt tv tecnology is not look good in moderns tv and monitors like jumping-blurry image) maybe if you reading this not understand many things but i intend update my tutorial about disable interleacing function in ps2 games i published in [PCSX2 forums](https://forums.pcsx2.net/Thread-No-interlacing-codes?pid=610584#pid610584) last year (still it need update some step not work anymere) i will update here and there too next weeks but lets talk about PAL version......

PAL version the game was more difficult because not have debug symbols, also load custom .elf (PS2 executable format) clear ps2 ram, load main .elf executable so finding codes will be more difficult, I find the 480p (hours of reasonings) but was messup by PAL FUNCTION so the main task i propose to me was rip off that PAL selector wich no required anymore with 480p mode (but still required if you live in europe playing with old crt TV PAL signal only :) )... i intend to explain better this posts but will be updated after ... meanwhile lets go with the goods.... i disable PAL mode, reenable native 480p progressive mode disable functions a no more interleaced signal enabled, i intent to name this codes for PAL ports (who many hate) the "Des-PAL-letizer" codes which take me some hours of thinking and testing.

## GAMES CODES:

### Assault Suits Valken (Europe) SLES_532.33;1) Game CRC = 0x1E177BBC

- +Des-PAL-Letizer code (disable call-function pal video selector)
- +Autoboot - Enable Native Progressive Scan video mode call-function
- +No interleacing (native progressive mode disable this)
- *recomended auto-profiles options for PCSX2-QT included in download
*pending code tag here

### Assault Suits Valken (Japan) 重装機兵ヴァルケン SLPM_625.01;1) Game CRC = 0x032CEF87
- +Autoboot - Enable Native Progressive Scan video mode call-function
- +No interleacing (native progressive mode disable this)
- *recomended auto-profiles options for PCSX2-QT included in download
*pending code tag here

##HOW TO USE:

## METHOD 1
### DOWNLOAD CODE FILES FOR PC EMULATOR "PCSX2-QT" FROM HERE:
[look and click -CODE>DOWNLOAD>ZIP> navigate in Playstation_2 folder](https://github.com/felixthecat1970/gamepatches)
*copy files and folders from "Assault Suits Valken (Japan) (Europe)" to your default PCX2-QT emulator !!!this overwrite any custom cheats / gameconfigs for the game in your emualtion.!!!
or download pnach files directly from PCSX2 forums post here: *pending link

## METHOD 2 
### APPLY/PATCH GAME DUMPS .BIN/CUE=cd or .ISO=DVD:
*pending tutorial
meanwhile use PS2 Patch Engine by pelvicthrustman 1.03 from here: [Link](https://www.psx-place.com/resources/ps2-patch-engine-by-pelvicthrustman.694/)
download .pnach codes from method 1, open pnach codes with text editor, copy to tool and patch you dump.

This codes enable best image mode support in PCSX2-QT emulator and PS2/PS3/PS4 Consoles, also you can test the correct pixel aspect ratios for "Integer Scaling" 2d (in pc emulation -*still untested i dont have 2k-4k nmonitors) learn more about it: [HERE](https://tanalin.com/en/articles/integer-scaling/) *Pending more detailed tutorial.

### TESTED setups:
- PC: - RYZEN 3400G WITH INTEGRATED GPU VEGA 11 + PCSX2-QT-avx2 
- PS3 SLIM (USA MODEL) - CFW evilnat 4.88 + webmanmod
- PS2 - (UNTESTED) *look How to play
- PS4 - (UNTESTED) *look How to play

### FAQ:
This codes is for ?
Use in PC emulator PCX2-QT, PS3 HARDWARE CONSOLES (hdmi-component 480p-720p-1080p setups only), PS2 HARDWARE CONSOLES (with component and progressive tv setups) incompactible with interleaced signals setups like rf, rca, white, red, yellow cables.

### This can be used with original game disks?
yes, but only in ps2 consoles and ps3 fat ps2 backward compactibility models like the 60gb-20gb USA/JAPAN only (Europe models is ps2 software emulation= bad compactibility/bugs) for ps2 use PS2 OPL homebrew cheats setup or gameshark devices (you need to convert codes which is hard) but more easy step is dump your game and patch it and have your console homebrew enabled. (**pending guide how to dump correctly) but more tech oriented /seasoned people here "how to dump correctly" [link](http://wiki.redump.org/index.php?title=Dumping_Guides) 

### How to play in...:
Recomended official developers - collaborators sites:
- PC: - [Playstation 2 official emulator site](https://pcsx2.net/)
- PS3: - [Official site for enable homebrew ps3xploit.com](http://ps3xploit.com/) [Official CFW Evilnat thread](https://www.psx-place.com/threads/4-89-evilnat-cfw-w-cobra-v8-3-cex-nobd-nobt-builds.37272/)
- PS2: - [Recomended guide for enable Hombrew](https://www.psx-place.com/threads/tutorial-the-great-ps2-aio-guide.30219/)
- PS4: - Need enabled homebrew console (posible all ps4 models with firmware 1-00 - 9.00)
- Need to create .PKG and install package use recomended tool by kozarovv [LINK](https://www.psx-place.com/threads/release-ps2-fpkg-0-6-by-jabu-new-tool-to-convert-ps2-games-for-ps4.30350/)
- For lastest news releases config parameters required for ps2 in ps4 emulation look here [LINK](https://www.psx-place.com/threads/research-ps2-emulator-configuration-on-ps4.16131/) 

## Disclaimer:
This is my findings, ideas, codes, information, experiments, deduction in a empirical manner, nothing is granted to work perfect or is correct information about code reverse enginnering. 