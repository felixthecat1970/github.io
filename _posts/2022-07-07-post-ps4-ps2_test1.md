---
classes: wide
title: "PS4 running PS2 software test"
excerpt_separator: "<!--more-->"
categories:
  - Blog
  - PS4
tags:
  - PS4
---

Here you will find testing some basics and interestings codemaking for run PS2 software in popular PS4 console. for games related info use old post.

<!--more-->

## Disclaimer:
This is my code finds, ideas, information, experiments, deduction in a empirical manner, nothing is granted to work perfect or is correct information about code reverse enginnering, for more tecnical approach i leave lectures in the end will help understand more, the next stories are related in a friendly, free, uncared manner for friends and people can someway understand. 

## CODE NOTES - STORIES:
I heard some years ago about ps4 port of PS2 game software, that time was thinking will be bad because complexity PS2 hardware desing so no take hopes in it (also i did not have a PS4 for test that time), so now after spends last coins in PS4 test setup months ago, recent homebrew deveplopment i take a look how it is PS2 running ps4 and yes is good very promissing; because the level of documentation spend some weeks learning (look lectures are tecnical information) but resume sony take bull by horns developing a custom scripted commands who try emulate or workaround many PS2 internals using PS4 cpu-gpu, the scripting is passed in LUA language (new to me more to learn) using same code created for PS2 emulation in PS3 and horsepower of PS4 (ps3 > ps4 comparation wise) giving for surprise amazings results games can run in HD enhaced internal resolutions (like PC), can use Qol features like saves, captures image - video (still 30fps) repacks, game manuals custom overlays, controller compactibilities etc and amazing custom scripting for more advanced codes i was testing in PS2 counterparts i would said same as PC emulation, so great but all is not simple, thanks to PS4DEVWIKI have a lot of documentation and still missing info about houndred commands to pass, test, debug; also using a networked setup with codemaking > copilation > network install > run more or less similar to developers in PS4 debug stations still is a lot of time spend so no way to think people using old school create, copy to usb > install .... so boresome; still i manage to learn and port some codes i did for PS2 and you can test here, if you are interested i leave page documentation in lectures so lets get started. Edit:also fixed some codes for old post related.

## GAMES CODES:
### Hokuto no Ken Shinpan no Sousousei Kengou Retsuden (Japan) CRC-0x9E8F0454 SLPM_666.60
- +Autoboot - Enable Native Progressive Scan video mode sdtv/480p
- +Disable soft image filter by default (can be eneabled - disabled any time L3=Off R3=ON)
- +Disable in game antialias, is not necessary anymore and causes graphic bugs
- +tests some ligths and arcade figthsticks compactibility (untested)
- +add some icon - background for build (zip download)

CLI:
```
#USE kof98 emu files
--gs-progressive=1
--gs-use-deferred-l2h=0
--hid-pad=1
--gs-uprender=none
--gs-upscale=point
```
---------------------------------------------------------------------------------------------

LUA:
```
--gametitle=Hokuto no Ken Shinpan no Sousousei Kengou Retsuden (Japan) CRC-0x9E8F0454 SLPM_666.60
--comment= PS4 port Native 480p sdtv mode + extend 640x480 v4 by felixthecat1970

apiRequest(2.0)	-- request version 0.1 API. Calling apiRequest() is mandatory.

local eeObj = getEEObject()
local emuObj = getEmuObject()
local gsObj	= getGsObject()

local lightDef0 = {153, 0, 0}
local lightDef1 = {0, 0, 153}

emuObj.PadSetLightBar(0, lightDef0, 1, lightDef1)

--//Native 480p sdtv mode + 640x480

local options = function()

eeObj.WriteMem32(0x20292720,0xA38286E8)
eeObj.WriteMem32(0x202ACA50,0x0000102D)
eeObj.WriteMem32(0x202B3EB8,0x0000102D)
eeObj.WriteMem32(0x202B4068,0x0000102D)
eeObj.WriteMem32(0x002B3D38,0x24060000)

end
emuObj.AddVsyncHook(options)

--soft filter L3=OFF R3=ON

local CheckInputs = function()

local pad_bits = emuObj.GetPad()
local UP		= pad_bits &  0x0010
local DOWN		= pad_bits &  0x0040
local LEFT		= pad_bits &  0x0080
local RIGHT		= pad_bits &  0x0020
local Triangle	= pad_bits &  0x1000
local Cross		= pad_bits &  0x4000
local Square	= pad_bits &  0x8000
local Circle	= pad_bits &  0x2000
local L1		= pad_bits &  0x0400
local L2		= pad_bits &  0x0100
local L3		= pad_bits &  0x0002
local R1		= pad_bits &  0x0800
local R2		= pad_bits &  0x0200
local R3		= pad_bits &  0x0004
local Select	= pad_bits &  0x0001
local Start		= pad_bits &  0x0008	

if (L3 ~= 0) then
	 gsObj.SetUpscaleMode("point")
	end
if (R3 ~= 0) then
     gsObj.SetUpscaleMode("gpu")
	end
end
emuObj.AddVsyncHook(CheckInputs)
```

### Sengoku Basara X (Japan) SLPM_550.08;1) Game CRC = 0x721DEBE4
- +Autoboot - Enable Native Progressive Scan video mode sdtv/480p
- +Disable soft image filter by default (can be eneabled - disabled any time L3=Off R3=ON)
- +Disable in game antialias, is not necessary anymore and causes graphic bugs
- +tests some ligths and arcade figthsticks compactibility (untested)
- +add some icon - background for build (zip download)

CLI:
```
#USE kof98 emu files
--gs-progressive=1
--gs-use-deferred-l2h=0
--hid-pad=1
--gs-uprender=none
--gs-upscale=point

```
----------------------------------------------------------------------------------------------------

LUA:
```
--gametitle=Sengoku Basara X (Japan) SLPM_550.08;1) Game CRC = 0x721DEBE4
--comment=PS4 port native sdtv 480p mode unlock + extend resolution 640x480 v4 by felixthecat1970

apiRequest(2.0)	-- request version 0.1 API. Calling apiRequest() is mandatory.

local eeObj = getEEObject()
local emuObj = getEmuObject()
local gsObj	= getGsObject()

local lightDef0 = {153, 0, 0}
local lightDef1 = {0, 0, 153}

emuObj.PadSetLightBar(0, lightDef0, 1, lightDef1)

--//Native 480p sdtv mode + 640x480

local options = function()

eeObj.WriteMem32(0x001004E4,0xA2620016)
eeObj.WriteMem32(0x0010CF00,0x24040000)
eeObj.WriteMem32(0x001EA6B4,0x24060000)
eeObj.WriteMem32(0x001EA6B4,0x24060000)
eeObj.WriteMem32(0x20386720,0x002A0640)
eeObj.WriteMem32(0x20386740,0x002A0640)
eeObj.WriteMem32(0x002A0550,0x24020000)
eeObj.WriteMem32(0x201EA7D0,0xAE0AFCB4)

end
emuObj.AddVsyncHook(options)

--soft filter L3=OFF R3=ON

local CheckInputs = function()

local pad_bits = emuObj.GetPad()
local UP		= pad_bits &  0x0010
local DOWN		= pad_bits &  0x0040
local LEFT		= pad_bits &  0x0080
local RIGHT		= pad_bits &  0x0020
local Triangle	= pad_bits &  0x1000
local Cross		= pad_bits &  0x4000
local Square	= pad_bits &  0x8000
local Circle	= pad_bits &  0x2000
local L1		= pad_bits &  0x0400
local L2		= pad_bits &  0x0100
local L3		= pad_bits &  0x0002
local R1		= pad_bits &  0x0800
local R2		= pad_bits &  0x0200
local R3		= pad_bits &  0x0004
local Select	= pad_bits &  0x0001
local Start		= pad_bits &  0x0008	

if (L3 ~= 0) then
	 gsObj.SetUpscaleMode("point")
	end
if (R3 ~= 0) then
     gsObj.SetUpscaleMode("gpu")
	end
end
emuObj.AddVsyncHook(CheckInputs)
```

This codes run PS2 games descripted in PS4, console has to be homebrew enabled for install, keep in mind due to emulation nature "maybe" games can have bugs in long plays.

## HOW TO USE:
### METHOD 1 - USE custom "CLI" and "LUA" configs for build PKG :
Use codes above with Kozarov's tool (Look in the end) for build custom .PKG package with SLPM-XXX.XX-CLI.txt and SLPM_XXX.XX.lua values  
Or click [download zip](https://github.com/felixthecat1970/gamepatches/archive/refs/heads/main.zip) > navigate to Playstation_4 folder use files match your game.

### TESTED setups:
- PS4 - Runs ok

## FAQ:
### This codes is for ? 
use in PS4 homebrew enabled consoles

### RECOMENDED LECTURES THANKS TO:
- https://www.psdevwiki.com/
    - URL: [- PS4 PS2 Emulation](https://www.psdevwiki.com/ps4/PS2_Emulation)
	
### How to play in...
Recomended official developers - collaborators sites:
- PS4:
    - Need enabled homebrew console (possible in all ps4 models with firmware 1-00 > 9.00)
    - Need to create .PKG and install package, use recomended tool by kozarovv [LINK](https://www.psx-place.com/threads/release-ps2-fpkg-0-6-by-jabu-new-tool-to-convert-ps2-games-for-ps4.30350/)
    - For lastest news releases config parameters required for ps2 in ps4 emulation look here [LINK](https://www.psx-place.com/threads/research-ps2-emulator-configuration-on-ps4.16131/)
