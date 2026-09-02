# Designing layout 
- Sun Aug 29th
- 1.5 hr

I spent time planning out what type of keyboard I want, features to implement, and the layout of the keys. 
I've decided I wanted features of a split-wired keyboard, row staggering, Alice curved, extra keys for shortcuts, gasket mount with 3 layers, mousebites on PCB, and a foldable keyboard stand.
I'm thinking of implementing LEDS, Hot-swaps, a keyboard strap, PETG instead of PLA, and some other aesthetics.

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



