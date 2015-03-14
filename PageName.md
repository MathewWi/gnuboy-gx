# Introduction #


GnuboyGX is a port for the Nintendo Gamecube and Nintendo Wii (running in GC mode)
of the open-source Gnuboy emulator, originally coded by Laguna and Gilgamesh.
More infos about Gnuboy here: http://en.wikipedia.org/wiki/Gnuboy

This port is based on the last 1.0.4 CVS source, released by Joshua_from EFNet #gameboy
http://www.netaxs.com/~gevaryah/gnuboy-1.0.4pre.tar.bz2._

This has nothing to do with the previous GX port for GCLinux, this is a full standalone
port using LibOGC API (GX, Audio, Inputs...)
See changelog.txt for the whole history.

If you have any questions about this, please contact us on the official GnuboyGX thread:
http://www.tehskeen.com/forums/showthread.php?t=4443


# [FEATURES ](.md) #

> . Gameboy and Gameboy Color emulation with sound
> . DVD & SDCARD support for rom loading
> . Freeze State support (load & save)
> . SRAM/RTC support (load & save)
> . support for 8MB roms
> . support for zipped (.zip) roms
> . support for alternate Mono Gameboy palettes
> . RTC synchro
> . Load/Save SRAM and FreezeState files (compressed) from/to Memory Card & SDCARD
> . SDLOAD or IPL reboot option
> . Wiimote/Nunchuk/Classic controller support (Wii version only)
> . Automatic SRAM/FreezeState
> . Video mode supported: 480i,480p & 576i (automatic detection)



# [REQUIREMENTS ](.md) #

**SoftMod and/or HardMod (to boot the dol/elf)** Zipped or not (.gb & .gbc) ROMS


-=[USER NOTES ](.md)=-

**gnuboy\_cube.dol is the Gamecube version of this program. You only need to load and run
this DOL on your GC or WII (in GC compatibility mode) using various methods (Bootable DVD, SDLOAD,...)
If you have no idea on how to load&run a DOL, please go here on follow the available guides:
http://modyawii.tehskeen.com/  (Booting Homebrew Section)**

**gnuboy\_wii.dol is the Wii version of the program. It has been compiled to work in Wii mode, featuring extra feature
such as Wiimote/Nunchuk & Classic controller support. To run this on your Wii, you will need to install the
Homebrew Channel (http://hbc.hackmii.com/). Once installed, rename gnuboy\_wii.dol as boot.dol and copy this file on your sdcard,
in /apps/gnuboy for example. Icon.png and meta.xml should also be placed in the same directory.**


ROMS can be loaded from a SDCARD, either through a SD-adapter in MCARD slot (Gamecube version only), or through the
native Wii SD slot (WIi version only). ROMS must be copied on your SDCARD in the following directory: /gnuboy/roms

ROMS can also be loaded from a ISO9660 DVD (currently, ONLY the Gamecube version support DVD loading) and you obviously
need a modchip. The maximal readable size is 1.35GB on Gamecube and 4.7GB on Wii (in GC compatible mode).


IMPORTANT: When putting roms either on DVD or SDCARD, it is recommended to use subdirectories as there is
> a limit of 1000 files per directory.



# [CONTROLS ](.md) #

 GAMECUBE PAD 

- Z Button let you come back to the menu when playing a game
- A is Gameboy Button A
- B is Gamenoy Button B
- START is Gameboy START Button
- Y is Gameboy SELECT Button

 WIIMOTE/NUNCHUK/CLASSIC 

- HOME Button let you come back to the menu when playing a game
- Gameboy Button A is Button 2 (WIIMOTE only), A (WIIMOTE+NUNCHUK) or B (CLASSIC)
- Gamenoy Button B is Button 1 (WIIMOTE only), B (WIIMOTE+NUNCHUK) or A (CLASSIC)
- Gameboy START Button is Button PLUS
- Gameboy SELECT Button is Button MINUS

# [MENU ](.md) #

Press A (or 1) or to select a menu item.
Press B (or 2) to go back from a sub-menu.


> Play Game :    Run the game you just loaded or return to game
> 
---



> Game Info :    Some informations about the ROM
> 
---



> Hard Reset:    Reset emulator
> 
---



> Load New Game:
> 
---


> . Load from DVD: DVD must be ISO9660 (GC mode only)
> . Load from Front SD: Wii mode only
> . Load from SDCARD (SLOTA or SLOTB): You have to use a SD adapter in a MC Slot

> When using SDCARD, roms must be initially placed in the /gnuboy/roms/ subdirectory

> In both cases, the maximum number of files per directory is 1000
> It is recommended to use subdirectories.
> Pressing B will make you going up one directory while navigating.


> Emulator Options:
> 
---


> . Aspect: let you modify the display aspect ratio:
> > - ORIGINAL: original ratio (1.11:1) & resolution
> > - SCALED: the original aspect ratio is maintaned but display is scaled to fit screen vertical height (default)
> > - STRETCH: display is stretched to fill the screen (640x480)


> . Filtering: Gnuboy can filter screen colors to make them look more washed out or faded
> > like on a real GBC. You can also allow this for Mono GB games by setting the value to "ALL"


> . Sprite Sorting: Enable/Disable sprites to be sorted and prioritized according to their x
> > coordinate when in DMG (Mono GB) mode.


> . Force Mono : For GBC games to run in Mono GB mode.

> . GBA Features: Unlock gba-only features in some cgb games (See Zelda Oracle's serie)

> . Palette: Display some colors in Mono GB (Try Kirby's palette)

> . RTC Synchro: enable RTC synchronization with current system clock on SRAM load

> . Auto SRAM: automatically load & save SRAM file when loading a new game or leaving application

> . Auto Freeze: automatically load & save FreezeState file when loading a new game or leaving application


> Memory Manager:
> 
---


> . SRAM Manager:  Let you load/save SRAM and RTC data from/to the selected device
> . STATE Manager: Let you load/save Savestate data from/to the selected device

> . Device: Let you choose the device to use: SDCARD or MCARD

> The size of the created files is variable and depends on the ROM type.

> IMPORTANT:

  1. when using NGC Memory Card in SLOTA, some mounting errors may occur. In this case,
> > remove and insert the Memory Card again before trying to save/load anything.


> 2/ when using SDCARD, the directory /gnuboy/saves is automatically created


The following options differ between WIi & GC version:

**GC version**

> Stop DVD Motor:
> 
---

> > Stop the the disc from spinning during playtime (GC mode only)



> SD/PSO RELOAD:
> 
---

> > go back to SD/PSO Loader


> SYSTEM REBOOT
> 
---

> > reboot the console.


**Wii version**


> Return to Loader:
> 
---

> > go back to TP Loader or Homebrew Channel


> System menu
> 
---

> > return to Wii System menu.



# [DEV NOTES ](.md) #

According to the GNU status of this project, the sourcecode MUST be included in any binary releases you made.
To recompile the sourcecode, you will need to have installed:

> . DevkitPPC environment
> . libOGC last sources

The sourcecode is maintaned under SVN and can be obtained from here: https://gnuboy-gx.bountysource.com/

If you have no idea on how to compile DOLs , please refer to this thread:
http://www.tehskeen.com/forums/showthread.php?t=2968.



# [CREDITS ](.md) #

Original Gnuboy Sourcecode: Laguna & Gilgamesh
1.04 CVS fixes: Joshua_from EFNet #gameboy
Generic LibOGC (GX,Sound,Inputs) & GUI display sourcecode: SoftDev
Gnuboy Porting Code, GUI & extra features: Eke-Eke
Mono Gameboy palettes addition: Askot
DevkitPPC from Dave Murphy (WinterMute)
LibOGC by Michael Wiedenbauer (shagkur),Dave Murphy (WinterMute) & others
ZLIB by Jean-loup Gailly_







# Details #

Add your content here.  Format your content with:
  * Text in **bold** or _italic_
  * Headings, paragraphs, and lists
  * Automatic links to other wiki pages