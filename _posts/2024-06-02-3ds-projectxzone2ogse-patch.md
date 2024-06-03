---
classes: wide
title: "3DS PROJECT X ZONE 2 Original game sound edition language patch"
excerpt_separator: "<!--more-->"
categories:
  - Blog
  - 3DS
tags:
  - 3DS
---

3DS custom patches for project x zone 2 original game sound edition for PC and consoles.

<!--more-->

More Info about [PROJECT X ZONE 2：BRAVE NEW WORLD オリジナルゲームサウンドエディション](https://projectxzone.fandom.com/wiki/Project_X_Zone_2)
Recomeded lectures in end of post

<figure class="third">
<a href="/gamepatches-blog/assets/images/pxz2ogse.jpg"><img src="/gamepatches-blog/assets/images/pxz2ogse.jpg"></a>
	<figcaption>3DS Original Game Covers</figcaption>
</figure>

## Disclaimer:
This is my code finds, ideas, information, experiments, deduction in a empirical manner, nothing is granted to work perfect or is correct information about code reverse enginnering, for more tecnical approach i leave lectures in the end will help understand more, the next stories are related in a friendly, free, uncared manner for friends and people can "someway" understand. 

## CODE NOTES - STORIES:
Demo gameplay: (no forget change youtube quality to 1080p/60fps)

<iframe width="560" height="315" src="https://www.youtube.com/embed/C7OIBbZ13-M?si=yCsx8Ew5g2C1qA7Y" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

3DS PROJECT X ZONE 2：BRAVE NEW WORLD オリジナルゲームサウンドエディション CTR-BXPJ-JPN  
[Officlal site japanese](https://pxz2.bn-ent.net/)  
[gamefaqs release info](https://gamefaqs.gamespot.com/3ds/146043-project-x-zone-2/data)  

Patch v2 by felixthecat1970:  
+Optional Patch for (BASE) build to English or German or Spanish Language with 1.2update "b1 language patch"
+Special edition original sound BGM in options for patched languages (unavailable in international versions)
-japanese version has not subtitled battle voices option implemented, so no available other langs
+Bonus DLC install file (available menu options from chapter 1)

Notes "b1 language patch":  
Japanese version has more updated files that other version, some diferent scripted files, and characters data give potential bugs, unstranslated parts or crashes, consider lang patch as beta (only tested till chapter 1 ongoing...).    

Many years ago i want to play this game version with original BGM but was japanese only, last months i was checking my old files scripts etc and find old leftovers mod translate in my archives (i not remember if i published this); checked and has a problem with the file version and the cyclopedia was in japanese only, corrected and repack with update, and add other languages; i start replaying this game till chapter 1 without bugs.

Requirements:  
-Base Build file: PXZ-2-OGSE (JPN) (V1.2) (BASE)  
 sha1:03908C3DF4F8665BF48D0F15A1C50AA4C9B52F43  
 link:(uploading.....)  
-Patch file: PATCH-PXZ2_OGSE_GER-SPA-ENGb1.7z  
 Link: (uploading.....)  

3ds console with Homebrew enabled [guide](https://3ds.hacks.guide/) or PC emulator app citra / lime  
3ds Fbi homebrew for .cia install or similar app  
7z decompressor program for unpack patch. [more info here](https://www.7-zip.org/7z.html)  
	
Install:   

1 - Decompress PATCH-PXZ2_OGSE_GER-SPA-ENGb1.7z   
2 - open 1-readme for detailed instructions or copy base build "PXZ-2-OGSE (JPN) (V1.2) (BASE)" file to "original" folder  
3 - Run desired lang and OS patch  
4 - check output folder for new created file  

Uninstall:  

2 - Use 3ds official unistall in 3ds options  

##FAQ:  
I using my cartridge dump / other dump etc crash bugs not work?  
Due encryption nature 3ds/cia dumps changes, file patch is not viable. 

I have Game USA\EUROPE version, what is the diference with this?  
This japan edition has the special edition BGM sountract in options for gameplay, also exclusive changes or unknow data not available for international versions.

Battle ending voices has not text?  
japanese version has not subtitled battle voices option, so no available other langs, already tested file hex swap but seems calls are coded disabled or unavailable for japanese versions, so require advanced code.bin dissasemble knowledge for debug.

Game crash in XXXX scene, battle or some part is not traslated ?  
still i have not replayed the game for bugs or unstranlated parts; try use BASE build (japanese only) for bypass crash. No time for spend debbuging, now searching for a job....

Citra \ lime PC emulator crash in XXXXX?  
sorry, not support for emulators.

i have my game cart game sound edition, how lang patch it?  
Due to encrytion / decryption nature, create a file patch for .3ds or .cia is not viable (file size should be equal base build), layered romFS option from luma is other alternative but still have bugs or not fully patch it, best option is install this patches over (BASE) provided file.

how about my japanese original game saves?  
!!backup it!! i recommend use 3DS OFFICIAL SAVE SYSTEM for create backup for your file saves or your favorite "save manager" homebrew, i not resposible for save corruption, bugs etc.

about DLC?  
Enables official dlc content APsp mode ("hard" mode) and other intems check "output" folder for file install.

about other languages Ita Fre etc?  
No time for spend debbuging other files, now searching for a job....

### RECOMENDED LECTURES THANKS TO:  
- Title of article: Nintendo 3DS Architecture - A Practical Analysis  
  - Author: Rodrigo Copetti  
  - URL: [web site official](https://www.copetti.org/writings/consoles/nintendo-3ds/)  
  - Date of publication: September 16, 2023  
  - Last modified: April 30, 2024  
	
- 3DS ROM Guides   
  - Read [3DS ROM Guides](https://github.com/ihaveamac/3DS-rom-tools/wiki) 