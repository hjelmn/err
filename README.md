This project contains all the files from my recreation of the Err LED sign. Included
in this repository are the current Kicad files.

The board is roughly based on the data available at:

https://hackaday.io/project/183827-reverse-engineering-the-mooninite-led-panels/details

with minor modifications (there could be errors-- if you find some please post a
PR with the fix):

 - Added a tactile switch to control the mode of the panel. The modes are off,
   light triggered, and various dimmed states but this can be changed by
   modifying the PIC firmware.
 - Added a barrel power input to support an external power supply. Added a
   circuit to disable the batter if an external power supply is connected. This
   circuit uses a P-channel MOSFET which closes the Batt+ when a voltage is
   detected on Vcc.
 - Added a battery pack connector and pads to solder on a battery.
 - Increased the LED driver voltage from 12v to 24v using boost regulator.
 - Changed the 5v regulator to a D2Pak style from the TO-220.
 - Added a 24 channel dimmable LED driver and rewired LEDs in chains of 6-8.
 - Changed to PIC16 to get I2C support but that is not needed with the LED
   controller chosen. It uses PWR so the originsl PIC12 is likely sufficient.

TODO:

 - Code for the microcontroller. Waiting on getting the parts before the code is
   finished.

The current version of the board costs roughly $85 to produce with LEDs from
China and parts sourced from the US.

To use this project download kicad and open the project.

The license for all of these files is GPLv3.
