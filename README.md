
Designed a Pocket-Piano, which is an 8-key mini synthesizer. Each key plays one note of a C major scale, from C4 to C5, and a knob shifts every key down or up an octave. It's built around a C XIAO RP2040 microcontroller and plays sound through a small buzzer.
This is a design stage. For the schematic on Kicad, I was able to create it through the project library and wired the 8 push buttons to pins D2 through D9, with each button's other side going to the ground, so no resistors were needed. The knob connects to the 3.3V, ground, and analog pin DO. The buzzer connects to pin D1 through a 100 Ω resistor. I used net labels instead of long wires, added power flags, marked unused pins as no connect, and got the light scroll wheel checked with 0 errors.
For the PCB layout, I made a 100 × 50 mm two-layer board with the 8 keys in a row along the bottom, the XIAO, knob, buzzer, and resistor along the top, and M3 mounting holes in all 4 corners. I routed the trace on the front layer via to send the knob signal under the board and flipped both layers with the ground copper.
Finally, for the case and firmware:
For the case, I imported the board's 3D model and worked on creating the 4 standoff screw holes so that it can be screwed on for the mounting holes, and a notch in the back. Also, a USB-C cable can reset XIAO. I also exported it as a STEP and STL for 3D printing.
For the firmware, I use Arduino, which wrote the code in 3 stages:
1. Compiling each one
2. Setting up the pins
3. Checking which keys are pressed and placing it
It's a note with tone and gives it a cooldown between notes so that no keys sound at the same time, and reads a note to switch between 3 octaves.

<img width="1630" height="816" alt="Screenshot 2026-10-25 215440" src="https://github.com/user-attachments/assets/1f4da62a-fbb2-4444-a949-13b32444f4b2" />
<img width="643" height="357" alt="Screenshot 2026-10-25 195554" src="https://github.com/user-attachments/assets/68ee8901-273f-4f48-bf89-c90cf1abdc44" />
<img width="643" height="357" alt="Screenshot 2026-10-25 195554" src="https://github.com/user-attachments/assets/7d599188-a31a-4807-bc46-8319ecc87b95" />
<img width="1630" height="816" alt="Screenshot 2026-10-25 215440" src="https://github.com/user-attachments/assets/ffb944a1-9138-445f-8c3b-685177f9aa0c" />
# Pocket-Piano
Creating a pocket piano, which is an 8-key mini synthesizer built around XIAO RP2040, with a potentiometer that shifts the octave and a small speaker that plays each note.

## How it works
Each of the 8 keys plays one note of a C major scale (C4 to C5). The knob switches between three octaves: lower, normal, and higher. The XIAO RP2040 reads the buttons and drives a passive buzzer with PWM.

## Schematic

## PCB


## Case
An open-top 3D-printed tray. The board sits on four standoffs and screws in with M3 screws. A notch in the back wall lets a USB-C cable reach the XIAO.

<img width="762" height="372" alt="Screenshot 2026-10-25 213117" src="https://github.com/user-attachments/assets/efd07170-af86-4475-ba04-6e8db981a24f" />

<img width="1236" height="735" alt="Screenshot 2026-10-25 183523" src="https://github.com/user-attachments/assets/bc78957b-3fe0-45cd-9883-1324e213ac7f" />
<img width="1111" height="544" alt="Screenshot 2026-10-25 192553" src="https://github.com/user-attachments/assets/1e4ed094-ddaa-4253-9b84-a2bcccb0f9e2" />
<img width="853" height="697" alt="Screenshot 2026-10-25 190018" src="https://github.com/user-attachments/assets/d9aa1f1b-4a0a-4e5f-9f48-2ded16e94f91" />

<img width="822" height="690" alt="Screenshot 2026-10-25 195823" src="https://github.com/user-attachments/assets/d7cafaf7-d186-4836-bfb1-ebb9d026e340" />
<img width="610" height="316" alt="Screenshot 2026-10-25 200445" src="https://github.com/user-attachments/assets/0fb1c609-79df-4d57-a247-d0f33797a155" />
