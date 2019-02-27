Infrared Remote Control
=======================
Here, we are reverse engineering some remote controls to find out the infrared protocol used in the remote controller.
Remote controllers used are attached below as figure.

Remote control 1 (Broadcasting Television remote controller):
![astro](https://github.com/Bennyaw/Infrared-remote-control/blob/master/doc/RemoteModelsPic/IMG_1713.JPG)

Remote control 2 (HITACHI CP-X2530WN Projector remote controller):
![r016f_board](https://github.com/Bennyaw/Infrared-remote-control/blob/master/doc/RemoteModelsPic/IMG_1726.JPG)
![r016f_shell](https://github.com/Bennyaw/Infrared-remote-control/blob/master/doc/RemoteModelsPic/IMG_1729.JPG)

Equipment
----------
1. Power supply
2. Multimeter
3. Oscilloscope
4. Kingst LA1002 Logic Analyzer (prefer Sigrok Logic Analyzer)

Infrared Communications
=======================
**Why wireless?**
Before the wireless technology came out, people were using wired communications to receive and transmit data. There was a lot
of constraints and inconveniences, for example, the further the distance between the transmitter and receiver, the longer the
wire should be, and also the cost will be higher too, and it will be multiplied up when there is more than 1 communications was
going on, also it could be very messy with all the wires flying everywhere.
So we have the wireless communications to make people's life easier.

**How to communicates**
Majority of the wireless communications is using infrared to communicate. The transmitter is a infrared LED, receiver will be a sensor
module. This module is to convert the raw signal to a clean signal for the protocol to decode it.

The figure below shows 2 signals, 'IR Detect' is the raw signal, 'IR Receiver' is the signal after modulation by the receiver. So the
signal from the Infrared LED is the raw signal, which is the signal 'IR Detect'. The LED will blink, in a frequency range of 34kHz to 40kHz, depends on the protocol used, to produce the signal and transmit to the receiver or sensor.
*Example of the wavefrom taken from [here](https://sigrok.org/gitweb/?p=sigrok-dumps.git;a=tree;hb=HEAD)*
![raw vs modulated]()



Procedure
---------
I will be directly working on the board, so a power supply of 3V is needed here. From the figure above, some soldering works
is done there for conveniences.

Infrared Protocols
------------------
