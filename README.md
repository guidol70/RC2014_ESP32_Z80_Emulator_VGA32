# RC2014_ESP32_Z80_Emulator_VGA32

![RC2014 Emulation on the VGA32](https://github.com/guidol70/RC2014_ESP32_Z80_Emulator_VGA32/blob/main/Pictures/RC2014_VGA32_initial_boot.jpg)

The CutDown / Jr-Version lacks the following Features of the original Emulator-Version:
- virtual GPIO-Support is missing
- Telnet-Support is missing
- SPIFFS-Support is missing
- Code-Fragments of TTGO T1/T2 are not included

The original version (without VGA32-Support) is available at<br/>
https://github.com/djbottrill/ESP32-Z80-Emulator

This VGA32-Port does use the FabGL-Terminal from<br/>
https://github.com/fdivitto/FabGL

Notes / Problems at this time:
- This Jr Version does compile only with ESP32-Core v1.0.6 (no v2.x.x)
- This Jr Version does in this initial version problem with the Keyboard (Enter/Return)
  maybe because of the /r /n handling against the FabGL-Terminal versus the normal serial-print-routine
  See "Serial input string function" around line 395
  So sometimes you have to hit Enter/Return again (double)
- Keyboard & Screen-Colors Config-Menu via F12-key
- Breakpoint GPIO-Switches sw1(26) & sw2 (27) may be incorect or non free GPIOs
