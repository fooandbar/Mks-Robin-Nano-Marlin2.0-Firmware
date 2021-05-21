# Mks-Robin-Nano-Marlin2.0-Firmware for Star A/LABISTS SX1 3D printer
## Features
The firmware of Selpic Star A/LABISTS SX1, based on [Marlin2.0.x](https://github.com/MarlinFirmware/Marlin) and [Marlin2.0-For-Robin-Nano](https://github.com/makerbase-mks/Mks-Robin-Nano-Marlin2.0-Firmware), supporting classical GUI and touch screen. If you have 3.5inch touch screen, the [LittlevGL](https://github.com/littlevgl/lvgl) is supported. This firmware requires [a TFT LCD](https://www.amazon.com/dp/B08SGN7WDV) and [a heated bed](https://www.amazon.co.jp/dp/B08TH7SVMH).

## LICENSE
This program is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version. see [LICENSE](https://github.com/fooandbar/Mks-Robin-Nano-Marlin2.0-Firmware-For-Selpic-Star-A.LABISTS-SX1/blob/master/LICENSE)

## NOTICE
1. Once this firmware is installed, you cannot revert to Selpic's original firmware.
2. This version does not support a laser engraving kit yet.
## Build
As the firmware is based on Marlin2.0.x which is built on the core of PlatformIO, the buid compiling steps are the same as Marlin2.0.x. You can directly using [PlatformIO Shell Commands](https://docs.platformio.org/en/latest/core/installation.html#piocore-install-shell-commands), or using IDEs contain built-in PlatformIO Core(CLI), for example, [VSCode](https://docs.platformio.org/en/latest/integration/ide/vscode.html#ide-vscode) and [Atom](https://docs.platformio.org/en/latest/integration/ide/atom.html). VSCode is recommended.

### Firmware Can be run with/without [an autoleveling sensor](https://www.thingiverse.com/thing:4831530) and [an filament runout sensor](https://www.thingiverse.com/thing:4848446).
#### With sensors.
1. Switch to [master](https://github.com/fooandbar/Mks-Robin-Nano-Marlin2.0-Firmware-For-Selpic-Star-A.LABISTS-SX1) branch.
2. Build firmware:
3. Update firmware:
   
- Enter the `.pio\build\mks_robin_nano35` directory, copy `Robin_nano35.bin` to the sd card, rename `Robin_nano35.bin` to `Robin_nano.bin` . The pre-built firmware can be found [here](https://github.com/fooandbar/Mks-Robin-Nano-Marlin2.0-Firmware/tree/master/Firmware/wBLTOUCH).
- Insert SD card to the motherboard, and you can see the update interface after power on.   

#### Without sensors.

1. Switch to [woBLTOUCH](https://github.com/fooandbar/Mks-Robin-Nano-Marlin2.0-Firmware-For-Selpic-Star-A.LABISTS-SX1/tree/woBLTOUCH) branch.
2. Build firmware:
3. Update firmware:
   
- Enter the `.pio\build\mks_robin_nano35` directory, copy `Robin_nano35.bin` to the sd card, rename `Robin_nano35.bin` to `Robin_nano.bin` . The pre-built firmware can be found [here](https://github.com/fooandbar/Mks-Robin-Nano-Marlin2.0-Firmware-For-Selpic-Star-A.LABISTS-SX1/tree/woBLTOUCH/Firmware/woBLTOUCH).
- Insert SD card to the motherboard, and you can see the update interface after power on.   

#### with 3.5inch touch screen.
Before replacing a touch screen, upgrade the firmware.
1. Switch to [master](https://github.com/fooandbar/Mks-Robin-Nano-Marlin2.0-Firmware-For-Selpic-Star-A.LABISTS-SX1) branch or [woBLTOUCH](https://github.com/fooandbar/Mks-Robin-Nano-Marlin2.0-Firmware-For-Selpic-Star-A.LABISTS-SX1/tree/woBLTOUCH) branch.
2. Build config.
- Configuation.h:
    //#define FILAMENT_RUNOUT_SENSOR
    //#define MKS_ROBIN_TFT24
    #define MKS_ROBIN_TFT35
    //#define TFT_COLOR_UI
    #define TFT_LVGL_UI
- Configuation_adv.h:
    //#define ADVANCED_PAUSE_FEATURE
3. Update firmware:     
- Enter the `.pio\build\mks_robin_nano35` directory, copy `assets` folder and  `Robin_nano35.bin` to the sd card, rename `Robin_nano35.bin` to `Robin_nano.bin` .
- Insert SD card to the motherboard, and you can see the update interface after power on.   
4. replace a touch screen.

## Setup
### an autoleveling sensor
* use `Z Probe Wizard`
    Main menu  > Configuration > Advanced Settings > Probe offsets > Z Probe Wizard
