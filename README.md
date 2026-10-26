# Pocket-Piano
Creating a pocket piano, which is an 8-key mini synthesizer built around XIAO RP2040, with a potentiometer that shifts the octave and a small speaker that plays each note.

## How it works
Each of the 8 keys plays one note of a C major scale (C4 to C5). The knob switches between three octaves: lower, normal, and higher. The XIAO RP2040 reads the buttons and drives a passive buzzer with PWM.

## Schematic
![Schematic](images/schematic.png)

## PCB
![PCB](images/pcb.png)
![PCB 3D](images/pcb-3d.png)

## Case
An open-top 3D-printed tray. The board sits on four standoffs and screws in with M3 screws. A notch in the back wall lets a USB-C cable reach the XIAO.

![Case](images/case.png)

## Files
- `pcb/` KiCad project and gerbers.zip
- `cad/` case (STEP and STL) and the PCB 3D model
- `firmware/main/main.ino` Arduino code
- `BOM.csv` parts list

## BOM
See [BOM.csv](BOM.csv). Estimated total: about $19 plus shipping.

## What I learned
[Write 2–3 sentences in your own words here]
