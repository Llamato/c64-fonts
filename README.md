# c64-fonts
 Fonts for the Commodore 64.

## Official
| Preview (Graphics Mode) | Download | Description | Author |
|:-------:|:--------:| ----------- |:------:|
| ![Preview of graphics mode for "c64.bin"](original/c64_graphics.png?raw=true "c64.bin (Graphics Mode)") [View text mode](original/c64_text.png?raw=true) | [c64.bin](original/c64.bin?raw=true) | Default Commodore 64/128 character set, as found on the MOS 901225-01. | Commodore |
| ![Preview of graphics mode for "c64_swedish.bin"](original/c64_swedish_graphics.png?raw=true "c64_swedish.bin (Graphics Mode)") [View text mode](original/c64_swedish_text.png?raw=true) | [c64_swedish.bin](original/c64_swedish.bin?raw=true) | Official Commodore 64 Swedish/Finnish character set with the å, ä and ö characters. Found on [Zimmers.net](http://www.zimmers.net/anonftp/pub/cbm/firmware/characters/); originally named "c64-swedish3.bin". | Commodore |
| ![Preview of graphics mode for "c64_swedish2.bin"](original/c64_swedish2_graphics.png?raw=true "c64_swedish2.bin (Graphics Mode)") [View text mode](original/c64_swedish2_text.png?raw=true) | [c64_swedish2.bin](original/c64_swedish2.bin?raw=true) | Similar to "c64_swedish.bin", but the Ä and Ö dots and the Å ring are wider. Found on [Zimmers.net](http://www.zimmers.net/anonftp/pub/cbm/firmware/characters/); originally named "c64-swedish4.bin". | Commodore |

## Custom
| Preview (Graphics Mode) | Download | Description | Author |
|:-------:|:--------:| ----------- |:------:|
| ![Preview of graphics mode for "aniron.bin"](custom/aniron_graphics.png?raw=true "aniron.bin (Graphics Mode)") [View text mode](custom/aniron_text.png?raw=true) | [aniron.bin](custom/aniron.bin?raw=true) | Aniron, a font inspired by Peter Jackson's Lord of the Rings and Hobbit trilogies. Includes upper and lowercase letters, numbers, and symbols.| [Patrick Mollohan](https://github.com/patrickmollohan) |
| ![Preview of graphics mode for "apple_ii.bin"](custom/apple_ii_graphics.png?raw=true "apple_ii.bin (Graphics Mode)") [View text mode](custom/apple_ii_text.png?raw=true) | [apple_ii.bin](custom/apple_ii.bin?raw=true) | Apple II/II+ font ported to the Commodore 64. Includes upper and lowercase letters, numbers, and symbols.| Apple + [Patrick Mollohan](https://github.com/patrickmollohan) |
| ![Preview of graphics mode for "aurebesh.bin"](custom/aurebesh_graphics.png?raw=true "aurebesh.bin (Graphics Mode)") [View text mode](custom/aurebesh_text.png?raw=true) | [aurebesh.bin](custom/aurebesh.bin?raw=true) | Custom font for the C64 based on [Aurebesh](https://starwars.fandom.com/wiki/Aurebesh/Legends), the main writing system depicted in Star Wars. Includes upper and lowercase letters (based on Legends rules), numbers, and symbols.| [Patrick Mollohan](https://github.com/patrickmollohan) |
| ![Preview of graphics mode for "comic_sans.bin"](custom/comic_sans_graphics.png?raw=true "comic_sans.bin (Graphics Mode)") [View text mode](custom/comic_sans_text.png?raw=true) | [comic_sans.bin](custom/comic_sans.bin?raw=true) | Either you love it or you hate it, there is no in-between. Comic Sans on the Commodore 64. Happy April Fool's Day! Includes upper and lowercase letters, numbers, and symbols.| [Patrick Mollohan](https://github.com/patrickmollohan) |
| ![Preview of graphics mode for "hachicro.bin"](custom/hachicro_graphics.png?raw=true "hachicro.bin (Graphics Mode)") [View text mode](custom/hachicro_text.png?raw=true) | [hachicro.bin](custom/hachicro.bin?raw=true) | Hachicro, a simplistic outline font. Includes upper and lowercase letters, numbers, and symbols.| [Patrick Mollohan](https://github.com/patrickmollohan) |
| ![Preview of graphics mode for "kauno.bin"](custom/kauno_graphics.png?raw=true "kauno.bin (Graphics Mode)") [View text mode](custom/kauno_text.png?raw=true) | [kauno.bin](custom/kauno.bin?raw=true) | A calligraphic font for the Commodore 64. Includes upper and lowercase letters, numbers, and symbols. Found on [Zimmers.net](http://www.zimmers.net/anonftp/pub/cbm/firmware/characters/). | Unknown |
| ![Preview of graphics mode for "kirby_forgotten_land.bin"](custom/kirby_forgotten_land_graphics.png?raw=true "kirby_forgotten_land.bin (Graphics Mode)") [View text mode](custom/kirby_forgotten_land_text.png?raw=true) | [kirby_forgotten_land.bin](custom/kirby_forgotten_land.bin?raw=true) | The in-game font extracted from Kirby and the Forgotten Land. Includes letters (uppercase only), numbers, and symbols. | [Patrick Mollohan](https://github.com/patrickmollohan) |
| ![Preview of graphics mode for "minecraft.bin"](custom/minecraft_graphics.png?raw=true "minecraft.bin (Graphics Mode)") [View text mode](custom/minecraft_text.png?raw=true) | [minecraft.bin](custom/minecraft.bin?raw=true) | A pixel-accurate port of the in-game font of Minecraft. Includes upper and lowercase letters, numbers, and symbols.| Mojang + [Patrick Mollohan](https://github.com/patrickmollohan) |
| ![Preview of graphics mode for "zx_spectrum.bin"](custom/zx_spectrum_graphics.png?raw=true "zx_spectrum.bin (Graphics Mode)") [View text mode](custom/zx_spectrum_text.png?raw=true) | [zx_spectrum.bin](custom/zx_spectrum.bin?raw=true) | The font, as found on the ZX Spectrum, ported to the Commodore 64. Includes upper and lowercase letters, numbers, and symbols.| Sinclair + [Patrick Mollohan](https://github.com/patrickmollohan) |

# Usage
## Using on Real Hardware
### Non permanent
Download and install [VICE](https://vice-emu.sourceforge.io/index.html#download) for your system. In the bin folder of your download, you will find a tool called c1541.exe. It is a file manager for d64 disk images we are going to use to pack the font into a disk image.

```
c1541 -format fonts,01 d64 c64fonts.d64 -attach c64fonts.d64 -write fontfilename fontfilenameondisk
```

After this command is finished a disk image file called c64fonts.d64 should be in the bin directory.

Next this image needs to be accessed with your c64. There are several tools for making d64 images available to a real c64. My personal favorite is the raspberry pi based cycle exact 1541 hardware emulator called pi1541. More information on that to be found here https://cbm-pi1541.firebaseapp.com/

Once we managed to transport our d64 file to a c64, we are almost done.
All that is needed now is a loader program to load the font into an appropriate memory location and tell the computer that we would like to use it.
Below you find a ready to use example loader program.


```basic
10 input "drive"; d
20 input "filename"; F$
30 poke 53272, peek(53272) and 240 or 14
40 sys7812 F$,d,0
50 poke 780, 0
60 poke 781, 2
70 poke 782,56
80 sys 65493
90 poke 55,0
100 poke 56,56

```

Now just enter drive letter of the drive containing the font file and the file name of the font file as prompted and there you go. Now you can use the c64 basic editor in a font of your choice.

To switch back to the default font simply restart your c64.

### permanent
Coming soon.

## Using on VICE
Download and install [VICE](https://vice-emu.sourceforge.io/index.html#download) for your system. Once installed, open x64 (faster) or x64sc (more accurate).

Go to "Preferences" -> "Settings ..." -> "Machine" -> "ROM", and under the "Machine ROMs" tab, point the "Chargen" field to the font you would like to select. You can either type in the path manually or use the "Browse ..." button.

Once you've selected the font you want, you can close out of the settings page. By default, the settings will not save once you exit the emulator. If you wish to make the font permanent, you can either click "Preferences" -> "Save settings" to save your settings manually, or go back to "Preferences" -> "Settings ..." and check the box that says "Save settings on exit". 

