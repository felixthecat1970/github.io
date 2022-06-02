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

Assault Suits Valken and (重装機兵ヴァルケン) for playstation 2 console, only released in Japan and Europe, here you will find codes for disable the interleaced function, enable disabled modes for 480p progressive scan display mode and recomended profiles for PC emualtor PCX2-QT.

More info about game: [Wikipedia](https://en.wikipedia.org/wiki/Assault_Suits_Valken)

<!--more-->

![alt](https://github.com/felixthecat1970/gamepatches-blog/blob/gh-pages/assets/images/felixthecat.png)

<!--![]Assault Suits Valken (Europe)  |     重装機兵ヴァルケン (Japan)
:-----------------------------:|:-----------------------------:
(https://github.com/felixthecat1970/gamepatches-blog/blob/gh-pages/assets/images/asv-eu.jpg)  |  ![](https://github.com/felixthecat1970/gamepatches-blog/blob/gh-pages/assets/images/asv-jp.jpg)-->

## Before start ....
Almost 2+ years withow Job and looking something to keep me thinking i decide to organize my old reverse enginnering codes of games i did last years and some i published in PCSX2 forums last year, returning after a year looking now thread and new advances in PCSX2 pc emulator, the people are active with new codes, hacks etc, and me lurking there to post something (also i have to train my mind because boredom and no stable jobs are killing me) happen to find about github code pages proyects etc, so i decided to organize buch of left over codes proyects etc update and put in easy platform where people can use it.

## CODE NOTES - STORIES:
Looking last year for improve games i find has debug symbols (the japanese version) enabled, so learning more and study I find interesting codes like sharp buffer address and interleacing functions but still no like it, after past weeks re-learning more how to interact with functions, mips registers etc, i find pattern the programers leave disabled or half enabled functions like progressive scan function, ree-nable the function and enable native 480p progressive code wich also disable natively the interleacing function (was required to old crt tv tecnology wich is not required anymore,) maybe if you reading this not understand many things but i intend update my tutorial about disable interleacing function in ps2 games i published here >>>>  last year; and update here and there too but lets talk about PAL version......

PAL version the game was more difficult because has not enabled debug symbols, also load custom .elf (PS2 executable format) clear ps2 ram, load main .elf so finding codes will be more difficult, but the main task i propose to me was rip off that PAL selector wich no required anymore (but still required if you live in europe playing with old crt TV PAL signal only :9  ) i intend to explain better this posts but will be updated after ... meanwhile lets go with the goods.... i rip off seletor also reeenable native 480p progressive mode disable functions a no more interleaced signal enabled, i intent to name this codes for PAL games ports (who many hate) the "des-PAL-letizer" codes for keep in mind.

## GAMES CODES:

### Assault Suits Valken (Europe) SLES_532.33;1) Game CRC = 0x1E177BBC

- +des-PAL-letizer code (rip off call-function pal video selector)
- +Autoboot - Enable Native Progressive Scan video mode call-function
- +No interleacing (native progressive mode disable this)
- *recomended profile for PCSX2-QT included in download

### Assault Suits Valken (Japan) 重装機兵ヴァルケン SLPM_625.01;1) Game CRC = 0x032CEF87
- +Autoboot - Enable Native Progressive Scan video mode call-function
- +No interleacing (native progressive mode disable this)
- *recomended profile for PCSX2-QT included in download

### DOWNLOAD PNACH CODES FOR PC EMULATOR PCSX2-QT FROM HERE:
[Repository with patches in github](https://github.com/felixthecat1970/gamepatches/tree/main/Playstation_2)

*copy folders cheats - gamesettings and files to your default PCX2-QT emulator 

This codes give better - stable image in PCSX2-QT emulator and ps2 / ps3 / ps4 hardware, also you can use the correct pixel aspect ratios for integer scaling 2d in 2k - 4k monitors (in pc emulator) ---pending new post about it-----

### HOW TO APPLY PERSONAL DUMPS TO BE PLAYED IN CONSOLES:
- --*pending tutorial---
meanwhile use PS2 Patch Engine by pelvicthrustman 1.03 from here:
[Link](https://www.psx-place.com/resources/ps2-patch-engine-by-pelvicthrustman.694/)
open pnach codes with text editor and copy to tool and patch you dump.

### TESTED setups:
- PC: - RYZEN 3400G WITH INTEGRATED GPU VEGA 11 + PCSX2-QT-avx2 
- PS3 SLIM (USA MODEL) - CFW evilnat 4.88 + webmanmod
- PS2 - (UNTESTED - *PENDING) *look faq
- PS4 - (UNTESTED - *PENDING) *look faq

### FAQ:
This codes is for ?
Use in PC emulator PCX2-QT, PS3 HARDWARE CONSOLES (hdmi-component 480p-1080p only), PS2 HARDWARE CONSOLES (with component and progressive tv setups) incompactible with interleaced signals setups like rca, white, red, yellow cables.

### How to play in:
recomended official developers - collaborators sites:
- PC: - [Playstation 2 official emulator site](https://pcsx2.net/)
- PS3: - [Official site for enable homebrew ps3xploit.com](http://ps3xploit.com/) and [Homebrew enabler CFW Evilnat thread](https://www.psx-place.com/threads/4-89-evilnat-cfw-w-cobra-v8-3-cex-nobd-nobt-builds.37272/)
- PS2: - [Recomended guide for enable Hombrew](https://www.psx-place.com/threads/tutorial-the-great-ps2-aio-guide.30219/)
- PS4: - require homebrew enabled console - missing recomended website but go this thread for new about ps2 emulation in ps4 [link](https://www.psx-place.com/threads/research-ps2-emulator-configuration-on-ps4.16131/)

## Disclaimer:
This is my findings, ideas, codes, information, experiments, deduction in a empirical manner, nothing is granted to work perfect or is correct information about code reverse enginnering. 


