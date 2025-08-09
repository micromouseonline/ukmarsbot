---
title: "Main Board"
nav_order: 2
parent: "Build Guide"
---

# Main Board

# UKMARSBOT assembly details for original and version 1.3a boards: using either the Arduino Nano processor board or the Cytron Maker Nano RP2040 processor board

## Main PCB assembly

This is the original main printed circuit board top and bottom: identified by UKMARSBOT 20190804A on the edge.

<img width="318" height="239" src="https://ukmars.org/ukmars/wp-content/uploads/2020/07/pcbtop.png"/>

<img width="318" height="239" src="https://ukmars.org/ukmars/wp-content/uploads/2020/07/pcbbottom.jpg"/>

Below is the v1.3a main printed circuit board top and bottom: identified by ukmars.org and V1.3a on the edge.

<img width="318" height="256" src="https://ukmars.org/ukmars/wp-content/uploads/2024/02/PCBtop-640x513.jpg"/>

<img width="318" height="311" src="https://ukmars.org/ukmars/wp-content/uploads/2024/02/PCBbottom-1-640x528.jpg"/>

The V1.3a board has these differences from the original board :

1.  Three cut outs to allow the sensor boards to mount line photosensors closer to the centre of the robot
2.  The PCB LED on pin D13 and its R9 load resistor are replaced by 2 additional power smoothing capacitors
3.  The 2 holes for the battery holder elastic band have been removed
4.  The components that support the Bluetooth connection have been repositioned

#### BUILD SEQUENCE

The majority of the build is the same for both boards but differences will be pointed out as necessary

Solder the parts in order of height e.g. resistors, diodes, ceramic capacitor, switches and motor driver then IC then sockets/headers and big capacitors. The pictures below will show you where things need to go.

- Solder in resistors R1 to R6  
    <br/>![](https://ukmars.org/ukmars/wp-content/uploads/2020/07/r1tor6.jpg)

Note that on the v1 version of the board, the R2 and R5 resistors have been offset to make soldering easier, and on the V1.3a board it is R2 and R3 that are offset

![](https://ukmars.org/ukmars/wp-content/uploads/2021/11/image-5-640x83.png)

It is helpful if you put all of these resistors in place from the top of the board before you start to solder, as this will avoid you getting solder into the PCB holes next to the one you are soldering in. Check that you have the correct value resistors in each place before you solder them in. You may want to hold these resistors in place with some Blu Tack so that they do not fall out while you solder them on the bottom side of the board.  
<br/>Do not worry if the ends of the resistors at the back edge of the board short out together e.g. between R1 and R2 or R2 and R3 etc up to R5 and R6, as they are connected anyway in the circuit. Clip off all the excess leads for each device as soon as you have soldered it in so that it does not get in the way of further soldering. If you are using the Cytron Maker Nano processor board you do not need to put in resistors R1, R2, R3, R4 and R5 but they will do no harm if they are there, but you do still need R6

If you are using the Arduino Nano processor, solder in R7 and R8 making sure that these 10K Ohm resistors which are mounted below the Arduino are close to the board. Note that the marking of the position of these varies slightly between the v1 and the v1.3a boards. These two components should be left out if you are using the Cytron Maker Nano RP2040 processor board

![](https://ukmars.org/ukmars/wp-content/uploads/2020/07/r7r8.jpg)

Now solder in the 2 diodes between the Arduino socket and the motor mounts. The larger one is to protect against the battery being connected the wrong way round, while the smaller one is used for the Bluetooth service (see blow). Make sure these are connected the right way round. The diagram is for the v1.3a board but the earlier board is similar with slightly different sized parts shown.

![](https://ukmars.org/ukmars/wp-content/uploads/2024/04/image.png)

![](https://ukmars.org/projects/ukmarsbot/ukmarsbot-build-guide/main-board/images/r7r8.jpg)If you plan to use an HC05 or HC06 or similar Bluetooth module for serial connection the v1 board has 2 extra resistors R10 and R11 and an extra diode D2. Note that on V1.3a these components are in a slightly different place and the diode is renamed as D3

Solder these 2.2K and 3.3K ohm resistors in as shown and then ensure that you put the diode in the right way round with the grey band at the end closest to the 3.3K resistor. Also add a 4 pin header for plugging the HC05 or HC06 module into, which if it has 6 pins should have one pin each side of the 4 way connector and oriented so that the 5v connection on the module aligns with the 5v shown on the board.

<img width="307" height="185" src="https://ukmars.org/ukmars/wp-content/uploads/2021/11/image-1.png"/>

<img width="174" height="240" src="https://ukmars.org/ukmars/wp-content/uploads/2024/02/bluetooth-2.jpg"/>

<br />
- Solder in the single row 15-way Arduino socket on the side of the motors – take care to connect all 15 pins and inspect it after soldering. A good tip is to solder just the 2 end pins first then check that it is fully seated and upright before soldering in the other 13 pins.  
    ![](https://ukmars.org/ukmars/wp-content/uploads/2020/07/socket15way.jpg)  
    
<br />
- Solder in the IC 74LS86N checking that the dot in the plastic by pin 1 and the notch at the end of the IC are at the end closest to resistors R7 and R8. You may need to bend the pins slightly inwards before it will go in smoothly.  
    Then put ceramic disc capacitor c1 in between the IC and resistor R8. You may need to allow enough length in the leads so that it can bend partly over R7 and R8 so that it stays below the level of the top of the Arduino connector.  
    <img width="290" height="175" src="https://ukmars.org/ukmars/wp-content/uploads/2020/07/ic74ls86n.jpg"/>     <img width="135" height="175" src="https://ukmars.org/ukmars/wp-content/uploads/2020/07/ceramiccapacitor.jpg"/>  
    
<br />
- Solder in the tactile switch S2 – It should only fit one way
<br />
- If you are using the Arduino Nano processor board, solder in the other 15 pin Arduino connector making sure it is fully seated and upright. Then add the 4-way DIPs switch S4  
    <img width="250" height="118" src="https://ukmars.org/ukmars/wp-content/uploads/2020/07/second15way.jpg"/> <img width="160" height="114" src="https://ukmars.org/ukmars/wp-content/uploads/2020/07/switchs2s4.jpg"/>  
    ![](https://ukmars.org/projects/ukmarsbot/ukmarsbot-build-guide/main-board/images/switchs2s4.jpg)If you are using the Cytron Maker Nano processor board, cut the 15 way connector into a 3-way and an 11-way one then solder in the 3 way one at the end nearest the 4 hole serial socket, then leave a one pin gap and put the 11 way socket in the rest of the holes in the board. Don’t put in the 4-way DIP switch but put a connecting wire between the bottom left and the top right of the socket holes. On the back of the board solder together the 5V and the adjacent 3.3V pins of the J1 sensor connector.
<br />
- View of modifications for Cytron Maker Nano board connector and 4 way switch socket
    
    <img width="196" height="124" src="https://ukmars.org/ukmars/wp-content/uploads/2024/07/cytronsocket.jpg"/>
    
    <img width="196" height="180" src="https://ukmars.org/ukmars/wp-content/uploads/2024/07/cytron4waysw.jpg"/>
    
<br />
- Add the two 6-way pin header connectors for the motors and the 14-way connector for the sensors. Placing the PCB down on a flat surface will help to get them seated fully while you solder these and the next ones in. You can either use pin headers (cut to length from a 36-way strip) or single row sockets as used for the Arduino (also cut to length from a 15-way item). If you are not using encoders on the motors you only need two 2-way headers soldered into the holes adjacent to where it says M1 and M2Add the 4 way pin header connector at the edge of the board next to R7 and R8 for the serial connection. Then solder the battery connector lead into the main PCB next to the on/off switch. On the v1 board solder the positive red lead into the centre one of the 3 holes marked + and the negative black lead into either of the two side ones marked – On the v1.3 board there are just 2 connections marked + and –  
    
<br />
- Add the miniature 3 pin slide switch used to switch the robot on and off – Yours may look slightly different to the one I have used, but as long as it is soldered into the 3 holes marked S1 that will be OK.  
    <img width="200" height="198" src="https://ukmars.org/ukmars/wp-content/uploads/2020/07/onoffswitch.jpg"/>  
    
<br />
- If your motor driver board or Arduino Nano does not have the headers soldered onto them do this now. Make sure that the short side of the pins are soldered onto the top side of the boards so that the black spacer and long pins are on the rear side of the board where there are no components.  
    
<br />
- Solder the motor driver board onto the main PCB so that the yellow tantalum capacitor on the motor driver board is at the end closest to where the Arduino Nano will be.
<br />
- For the original and V1 board, solder in R9 1kὨ resistor next to the motor driver board and then add a 2 or 3mm indicator LED next to R9. The long lead on the LED (the +) should be the one furthest away from R9 and closest to the word LED on the board.  
    <img width="150" height="201" src="https://ukmars.org/ukmars/wp-content/uploads/2020/07/motordriverboard.jpg"/> <img width="350" height="195" src="https://ukmars.org/ukmars/wp-content/uploads/2020/07/r9andled.jpg"/>
    <br />

- For the V1.3a board add the two 470µF C2 and C3 smoothing capacitors using low items (12mm or less high) which will allow the USB mini connection lead to go over the top of it into the Arduino Nano. Make sure that the negative sides of the capacitors go on the white section of the component outline on the PCB
<img width="238" height="306" src="https://ukmars.org/ukmars/wp-content/uploads/2024/02/image-496x640.png"/>