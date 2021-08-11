# Robot PCB

In this project, I have given a task to design a motherboard which should be compatible with all robots we have made so far in our training which are:
- Fighting Robot
- Serving Robot
- Evaluation Robot

So, in order to make the motherboard compatible with all those robots, I have made some decisions in my design which are:
- For power circuit, we can use either LM2596 DC to DC converter or NCP1117 voltage regulator, since both ATMega328p and WEMOS D1 MINI 32 could be powered by 5V so we will need only for converter or regulator, in my schematic I attached both circuits but in my PCB design I used LM2596 DC to DC converter.
- For power input I did not use the usual pins, I replaced them with 282837-2 connector by TE Connectivity, which in my has 2-positions and more stable.

<p align="center">
<img src="https://user-images.githubusercontent.com/85786699/128953014-1d79cd0d-2d50-4ff4-8466-528f45807908.png">
<br> 
Figure 1: 282837-2 connector</p>


- I designed the PCB to work using both ATMega328p and WEMOS D1 MINI 32 but I did not connect the TX and RX on the PCB, so  in our applications we will not be limited to the serial communication between the WEMOS ESP and ATMega328p since connecting them will limit some of WEMOS ESP functionality.
- I did not add ATMega328p bootloader circuit and also one of the reasons for using ATMega328p is we do not need to implement internal bootloader circuit into our PCB. Instead, we can implement one separate bootloader circuit to set up the ATMega328p then soldering install it into our PCB since we do not need to solder it into our separate bootloader circuit.


<p align="center">
<img src="https://user-images.githubusercontent.com/85786699/128955386-d502ef47-6ede-4856-9ea6-780419d43a72.png">
<br> 
Figure 2: Schematic for ATMega328p bootloader circuit</p>



**Note: this is my first PCB design and because there is not enough time before the end of this training to learn designing PCB's efficiently I was only learning for two days so I could not learned designing efficient PCB's, so there are a lot of VIA holes in my design and I did not change the width of the high current traces to improve thermal efficiency, but I did my best in this short period of time to learn and implement this PCB.**


# Schematic

<p align="center">
<img src="https://user-images.githubusercontent.com/85786699/128953607-8835c094-e68d-4999-93c8-b860b384437b.png">
<br> 
Figure 3: Schematic for my PCB design</p>



# 3D View for PCB


<p align="center">
<img src="https://user-images.githubusercontent.com/85786699/128953854-862f7a27-ed8b-4ca7-9c9b-6421d0033912.png">
<br> 
Figure 4: 3D view for my PCB design</p>


