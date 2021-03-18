# A-D-Conversion-with-ATmega328P-Lab-4-
In this lab you will create a circuit that can be used to control the speed of a DC motor (but we will not connect the motor in this lab) in five discrete steps: forward and backward slow, forward and backward fast, and stopped. The purpose of this lab is to read an analog sensor that will eventually be used to manually set the motor speed. You will use LEDs to indicate the speed setting of the motor.

Part 1 (circuit): Parts needed:
ATmega328P minimal circuit components
10kΩ resistors (1)
220Ω or 330Ω resistors (5)
Connector wires
Potentiometer or Photoresistor or RTD LEDs (5) – three different colors work best Multimeter

Start with the minimal ATmega328P circuit from Lab 1. Add five active-low LEDs on PORTB (because we’ll be using the A/D converter function of port C). It is helpful but not necessary to use three colors of LEDs: two on each end of different colors and a third color for the middle LED in the row.
Connect a sensor that provides an analog signal (e.g. a potentiometer). We could use a photoresistor or RTD (see Figure 1) but a potentiometer is easy to debug.). Wire the potentiometer as shown in Figure 2 so that the output voltage can be adjusted from 0 to 5V. Even though the input impedance of the A/D converter is high, it is a good idea to put a 10K resistor between the microcontroller’s A/D pin and the potentiometer.

Part 3 (code): Program your microcontroller such that the following motor control settings are achieved:
- There will be five motor speed settings: stopped, forward slow, backward slow,
forward fast, and backward fast.
- The motor speed settings will be determined based on the position of the
potentiometer. Divide the output voltage range of the potentiometer into five subranges of approximately 1 volt each. Motor speed is to be set as:
o The lowest voltage range corresponds to fast backward motor speed. o The second voltage range corresponds to slow backward motor speed. o The middle voltage range corresponds to a stopped motor.
o The fourth voltage range corresponds to slow forward motor speed.
o The highest voltage range corresponds to fast forward motor speed.
- The LEDs must match the motor speeds:
o Center LED is on when the motor is stopped
o An outer LED is on when motor is moving fast (one for forward and one
for backward)
o An inner LEDs is on when the motor is moving slowly (one for forward
and one for backward)
