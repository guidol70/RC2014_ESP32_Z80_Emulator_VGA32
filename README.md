# RC2014 ESP32Z80 V2 Emulator for TTGO VGA32

- Not Boot without a SDCard
![No Boot without a SDCard](https://github.com/guidol70/RC2014_ESP32_Z80_Emulator_VGA32/blob/main/Pictures/RC2014_VGA32_NoBoot.jpg)

- Booting with SDCard
![Booting with SDCard](https://github.com/guidol70/RC2014_ESP32_Z80_Emulator_VGA32/blob/main/Pictures/RC2014_VGA32_Boot.jpg)

-Showing the DiskSpace of the A: (A.dsk) Image-File
![SHowing the DiskSpace](https://github.com/guidol70/RC2014_ESP32_Z80_Emulator_VGA32/blob/main/Pictures/RC2014_VGA32_DiskSpace.jpg)

- Executing Wordstar 4.0
![Executing Wordstar](https://github.com/guidol70/RC2014_ESP32_Z80_Emulator_VGA32/blob/main/Pictures/RC2014_VGA32_Wordstar.jpg)

The Jr-cutDown-Version lacks the following Features of the original Emulator-Version:
- virtual GPIO-Support is missing
- Telnet-Support is missing
- SPIFFS-Support is missing
- Code-Fragments of TTGO T1/T2 are not included
BUT
SDCard-Support-Commands like sdfiles and sdcopy does work ;)

The original version (without VGA32-Support) is available at<br/>
https://github.com/djbottrill/ESP32-Z80-Emulator

This VGA32-Port does use the FabGL-Terminal from Fabrizio Di Vittorio (fdivitto2013@gmail.com)<br/>
https://github.com/fdivitto/FabGL

![VGATextColor_1](https://github.com/guidol70/RC2014_ESP32_Z80_Emulator_VGA32/blob/main/Pictures/ESP32Z80_VGAText_1.jpg)

![VGATextColor_2](https://github.com/guidol70/RC2014_ESP32_Z80_Emulator_VGA32/blob/main/Pictures/ESP32Z80_VGAText_2.jpg)

Notes / Problems at this time:
- Breakpoint GPIO-Switches sw1(26) & sw2 (27) may be incorect or non free GPIOs
- Config of Keyboard and Screen-Color via .ino because I had to use FabGL TextController
  instead the VGA16-Controller (got Problems to get the SDCard to init)

- CPMTool DiskDef for A: (A.dsk) Image-File:

```
# esp32z80
diskdef esp32z80
  seclen 512
  tracks 512
  sectrk 32
  blocksize 4096
  maxdir 512
  boottrk 0
  os 2.2
end
```
