# Designing layout 
- Sun Aug 29th
- 1.5 hr

I spent time planning out what type of keyboard I want, features to implement, and the layout of the keys. 
I've decided I wanted features of a split-wired keyboard, row staggering, Alice curved, extra keys for shortcuts, gasket mount with 3 layers, mousebites on PCB, and a foldable keyboard stand.
I'm thinking of implementing LEDS, Hot-swaps, a keyboard strap, PETG instead of PLA, and some other aesthetics.
Some things I want to change and work on from my previous keyboard design are: Use less PCB space, use less space for the keyboard on unnecessary things, and don't add extra colours / designs on the top / bottom case. These reasons are because of mainly cost, aesthetics and looks, and just in general how useless to is to have a bigger keyboard.

<img width="512" height="698" alt="image" src="https://github.com/user-attachments/assets/0d780c20-dd6a-4727-859e-88c82f279638" />

In this photo, I sketched out what the layout of my keys should be like. I also included a rotary encoder in the top left for probably brightness or volume. Afterwards, I wanted to switch to a curved Alice keyboard instead of a original Alice.

<img width="1116" height="810" alt="image" src="https://github.com/user-attachments/assets/13bde227-23d3-4969-af57-c7d156a3b503" />
These are the two types side by side. 

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# Designing Schematics
- Tue Sep 1 
- 3 hr

When making schematics I had to download marbastlib and panelization.pretty for 3d models and footprints. These libraries were used for switches, stabilizers, rotary encoder switch, and mousebites. Afterwards, I started to work on symbols and traces. Overall, designing schematics was not difficult, but just time-consuming because of designing the matrix for the switches and then fixing bugs in the Electric Rules Checker in Inspect tab. 

Working on the TRRS Jack (an audio port) as my interconnect cable, it was overall easy to add into as there only 4 points: Tip, Ring, Ring, Sleeve. Or known as Ground, VCC (5V or 3.3V), SERIAL as a Net Label, then Ground. Here's a picture of the microcontroller and TRRS Jack.
<img width="2186" height="588" alt="image" src="https://github.com/user-attachments/assets/2ff9238b-88b3-4b01-8dd8-0a1bc8a6037e" />

Here's a picture of the left side of the keyboard
<img width="1456" height="1378" alt="image" src="https://github.com/user-attachments/assets/f5d72aac-f432-4d68-a3ab-c4d4442c795c" />

Right side
<img width="1436" height="1228" alt="image" src="https://github.com/user-attachments/assets/3244c5a7-e0fc-426d-ad6f-3fdad745d330" />

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# Fixing Schematics + Assigning Footprints
 - Fri Sep 4
 - 1.5 hr

 I spent time after the last post to assigning footprints to the symbols and fixing schematic bugs. In the matrix, I fixed one switch by pushing it up a row because in the layout it was supposed to be one of the arrow keys, instead it was on an empty space.
<img width="1468" height="956" alt="image" src="https://github.com/user-attachments/assets/476fe8a8-3962-4b69-949d-fc339e91710d" />

Afterwards, I edited the TRRS Jack symbol pins from S, R1, R2, T, to 4, 3, 2, 1. The reason I did this was because when assigning footprints and updating PCB from Schematics, it gave me a huge amount of errors + warnings about the pins from the footprints and schematics being different. All I did was go into symbol editor for both TRRS Jacks and switched the pins. 
<img width="1966" height="1050" alt="image" src="https://github.com/user-attachments/assets/324e8708-a670-47fa-b63a-e68404390e9a" />

The footprint in PCB:
<img width="504" height="1020" alt="image" src="https://github.com/user-attachments/assets/aef91f99-198d-492a-914c-507e479bcf41" />

When finished, I just assigned all the footprints to the symbols. 

RaspberryPi_Pico - Module:RaspberryPi_Pico_Common_THT, 

Mousebite - Panelization.pretty-master:mouse-bite-5mm-slot, 

1N4148 - Diode_THT:D_DO-35_SOD27_P7.62mm_Horizontal, 

AudioJack4 - Keebio-Parts.pretty-master:TRRS-PJ-320A,

MX_stab - PCM_marbastlib-mx:STAB_MX_2u, 

RotaryEncoder_Switch - Rotary_Encoder:RotaryEncoder_Alps_EC11E-Switch_Vertical_H20mm, 

SW_Push - Button_Switch_Keyoard:SW_Cherry_MX_1.00u_PCB

This is a picture of updating the PCB from schematics:
<img width="1692" height="1302" alt="image" src="https://github.com/user-attachments/assets/fb6297fa-2937-434e-aaaf-1ca130201e0d" />


 


 

