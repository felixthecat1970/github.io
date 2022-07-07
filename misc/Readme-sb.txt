By FelixTheCat1970

v1 -initial
v2 -disable antialias by default because not necessary and cause graphic bugs
   -port codes and config info for PS2 to PS4 build

### Sengoku Basara X (戦国BASARA X) (Japan) SLES_532.33;1)
Chages:
- +Autoboot - Enable Native Progressive Scan video mode (call-function)
- +No interleacing (of course sdtv mode call disable it)
- +640x480 pixels-lines enabled (instead default 640x448) more viewable area, also for Integer scaling (still untested)
- disable antialias by default because not necessary and cause graphic bugs

!!! This only work in progressive signal TV|Monitors setups !!!
Ps2: with component cables - progresive signal setups
Ps3 backward ps2 hardware compactible models: component - hdmi cables, with 480p-720p-1080p modes

download readme for instructions or visit this link more info https://felixthecat1970.github.io/gamepatches-blog/blog/ps2/post-ps2-sb-hk/

How to patch:
1. use PS2 Patch Engine tool by pelvicthrustman 1.03 from here:
https://www.psx-place.com/resources/ps2-patch-engine-by-pelvicthrustman.694/

2. Copy "patch" lines to tool according your game version, select:
-Browse your game dump
-patch > format> "PNACH"
-copy "patch" lines according your game version
-patch and test.

-Sengoku Basara X (戦国BASARA X) (Japan) SLPM_550.08;1) 

patch=0,EE,201004E4,extended,A2620016
patch=0,EE,0010CF00,extended,24040000
patch=0,EE,001EA6B4,extended,24060000
patch=0,EE,202FAF88,extended,A0800014


!!!disable antialias option in game menu for 640x480!!!

Database match: redump.org
Sengoku Basara X
戦国ＢＡＳＡＲＡ　Ｘ（クロス）- SLPM 55008
SHA1: 5e31412d81f8c101c528473400f5cb9099202355

PS2 to PS4
visit link for code instructions:
https://felixthecat1970.github.io/gamepatches-blog/blog/ps4/post-ps4-ps2_test1/