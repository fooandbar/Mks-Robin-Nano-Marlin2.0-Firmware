# How to install

1. copy `Robin_nano.bin` to the sd card. 
2. Insert SD card to the motherboard, and you can see the update interface after power on.   

# Setup
## an autoleveling sensor
* use `Z Probe Wizard`
    Main menu  > Configuration > Advanced Settings > Probe offsets > Z Probe Wizard

# Linear Advance
see https://marlinfw.org/docs/features/lin_advance.html
1. unzip [an attached zip : Kfactor0.0-2.0.zip](https://github.com/fooandbar/Mks-Robin-Nano-Marlin2.0-Firmware-For-Selpic-Star-A.LABISTS-SX1/files/6641819/Kfactor0.0-2.0.zip).
2. print gcode. K increases by 0.2 for every 5 mm.

    <img src='https://user-images.githubusercontent.com/63621440/121769127-d3949980-cb9c-11eb-99a7-c153cadb80c1.png' width=200 />
3. set K factor.

    1. push Setting button.
    2. select `configuration` -> `Advanced configuration` -> `Filament` -> `Advanced K`
    3. set K factor.

# [Backlash compensation](https://marlinfw.org/docs/gcode/M425.html)
see https://www.thingiverse.com/thing:2040624 thanks!

1. unzip [an attached zip](https://github.com/fooandbar/Mks-Robin-Nano-Marlin2.0-Firmware-For-Selpic-Star-A.LABISTS-SX1/files/6641966/QuickBacklash20.zip)
2. slice a stl file to gcode.
3. print a gcode file.
4. set a backlash value.

    1. push Setting button.
    2. select `Configuration` -> `Advanced configuration` -> `Backlash`
    3. set X/Y distance value.
    4. set `Correction` to 100%.

