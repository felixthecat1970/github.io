---
classes: wide
title: "PS4 Homebrew convert PS2 games to play in it"
excerpt_separator: "<!--more-->"
categories:
  - Blog
  - PS4
tags:
  - PS4
---

Here you will find basic tools steps how to patch your PS2 games for run in PS4 (Homebrew enabled console).

<!--more-->

***Updated more easy tool

## Disclaimer:
This is my code finds, ideas, information, experiments, deduction in a empirical manner, nothing is granted to work perfect or is correct information about code reverse enginnering, for more tecnical approach i leave lectures in the end will help understand more, the next stories are related in a friendly, free, uncared manner for friends and people can someway understand. 

## NOTES
Sometimes you will find automated builds PS4 with my patches it takes many hours to make it works ok but i do not do all games, so here you will find tools make your ps4 builds too)
keep in mind PS4 > PS2 emulation still is experimental expec bugs, problems etc, each game has specific config or fixes, your only line of learn is [Research PS2 emulator configuration on PS4](https://www.psx-place.com/threads/research-ps2-emulator-configuration-on-ps4.16131/) search for configs, help there.

## WHAT TOOLS YOU NEEED?

1-PS4 Hombrew enabled console (till 2023 only models firmware 9.00 and backwards are compactible)  
2-PC with windows OS 10 / 11  
3-Have already you PS2 .iso or .bin/.cue game dump  
4-My update [codes - patch list online](https://docs.google.com/spreadsheets/d/e/2PACX-1vQK9yHshfnqIwf66Xb0MIG_hJ44fhPuBByI7jE8-OGSC1M63CN-bPFUbwBu9AUpl9n1wlt3oqIxcgEC/pubhtml?gid=0&single=true) Look PNACH files for codes  
5-optional Tool for patch PS2 games [PS2 Patch engine by pelvicthrustman](https://www.psx-place.com/resources/ps2-patch-engine-by-pelvicthrustman.694/) patch games with codes for easy life.  
6-Download new tool for convert Ps2 games to PS4 instalable PKG [PS2-FPKG v0.7-Beta by Jabu](https://www.psx-place.com/threads/release-ps2-fpkg-v0-7-beta-a-complete-rewrite-of-my-ps2-to-ps4-converter.41916/#post-374371)   

Following steps and some luck you game will work, but if not you need customs configs, lua patches etc, check advised forum [Research PS2 emulator configuration on PS4](https://www.psx-place.com/threads/research-ps2-emulator-configuration-on-ps4.16131/) for help, configs etc.

## CODE NOTES - STORIES:
I heard some years ago about ps4 port of PS2 game software, that time was thinking will be bad because complexity PS2 hardware desing so no take hopes in it (also i did not have a PS4 for test that time), so now after spends last coins in PS4 test setup months ago, recent homebrew deveplopment i take a look how it is PS2 running ps4 and yes is good very promissing; because the level of documentation spend some weeks learning (look lectures are tecnical information) but resume sony take bull by horns developing a custom scripted commands who try emulate or workaround many PS2 internals using PS4 cpu-gpu, the scripting is passed in LUA language (new to me more to learn) using same code created for PS2 emulation in PS3 and horsepower of PS4 (ps3 > ps4 comparation wise) giving for surprise amazings results games can run in HD enhaced internal resolutions (like PC), can use Qol features like saves, captures image - video (still 30fps) repacks, game manuals custom overlays, controller compactibilities etc and amazing custom scripting for more advanced codes i was testing in PS2 counterparts i would said same as PC emulation, so great but all is not simple, thanks to PS4DEVWIKI have a lot of documentation and still missing info about houndred commands to pass, test, debug; also using a networked setup with codemaking > copilation > network install > run more or less similar to developers in PS4 debug stations still is a lot of time spend so no way to think people using old school create, copy to usb > install .... so boresome; still i manage to learn and port some codes i did for PS2 and you can test here, if you are interested i leave page documentation in lectures so lets get started.

## FAQ:

### This codes is for ? 
use in PS4 homebrew enabled consoles

### My game crash, not work, bugs, how to, help, etc ? 
go here [PS2 Patch engine by pelvicthrustman](https://www.psx-place.com/resources/ps2-patch-engine-by-pelvicthrustman.694/)

### I need more info to learn?
check "LECTURES" next

### RECOMENDED LECTURES THANKS TO:
- https://www.psdevwiki.com/
    - URL: [- Devwiki PS4 PS2 Emulation](https://www.psdevwiki.com/ps4/PS2_Emulation)
	
