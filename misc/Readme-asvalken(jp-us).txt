By FelixTheCat1970

v1

Assault Suits Valken and (重装機兵ヴァルケン) for playstation 2 console, only released in Japan and Europe, here you will find patch for disable the interleaced function, disable PAL MODES, enable native 480p progressive scan display mode.

Changes:
+Des-PAL-Letizer code (disable PAL video selector screen)
+Autoboot - Enable Native Progressive Scan video mode (call-function)
+No interleacing

!!! This only work in progressive signal TV|Monitors setups !!!
Ps2: with component cables - progresive signal setups
Ps3: component - hdmi cables, with 480p-720p-1080p modes

download readme for instructions or visit this link more info.

How to patch:
1. use PS2 Patch Engine tool by pelvicthrustman 1.03 from here:
https://www.psx-place.com/resources/ps2-patch-engine-by-pelvicthrustman.694/

2. Copy "patch" lines to tool according your game version, select:
-Browse your game dump
-patch > format> "PNACH"
-copy "patch" lines according your game version
-patch and test.

-Assault Suits Valken (Europe) SLES_532.33 !!! (when promted patch to SLES_532.33)

patch=0,EE,2011D908,extended,00000000
patch=1,EE,2020FB0C,extended,24050004
patch=1,EE,2020FB10,extended,240701C0
patch=1,EE,2020BA40,extended,6466013E
patch=1,EE,2020BA44,extended,24A30033

-Assault Suits Valken (Japan) 重装機兵ヴァルケン SLPM_625.01

patch=0,EE,201C53FC,extended,240701C0
patch=0,EE,201C5410,extended,24050004
patch=0,EE,201E2D14,extended,65E3013E
patch=0,EE,201E2D18,extended,25C50033

More info about here: https://felixthecat1970.github.io/gamepatches-blog/blog/ps2/post-standard/

Database match: redump.org
Assault Suits Valken (Europe) SLES_532.33
SHA1: CE68CBB53124AD61ABF26EC5536116D41632F7FD

Assault Suits Valken (Japan) 重装機兵ヴァルケン SLPM_625.01
SHA1: C2F0B59AF6C7343BF16F805EBF427AE1339B2D6C