crt-driver
==========

This repository contains a circuit designed for driving electrostatic CRTs.
For additional details on the circuit see http://tubetime.us/?p=183.
There are several boards in this design:

1. 1KV Power Supply
  This board takes a 12V input and steps it up to approximately 800V-1200V.
  The circuit can source several milliamps so be extremely cautious while
  using it to prevent nasty electric shocks. Voltages this high with even
  just a few milliamps can stop your heart!

2. Electrostatic CRT Deflection and Video Amplifier
  The heart of the circuit is this board. It has two fully differential
  high voltage amplifiers/level shifters to drive the deflection plates,
  and a high-speed video amplifier (approx. 6MHz bandwidth) driving the
  CRT cathode. The input signals are all 3.3V analog. You may drive the
  video amplifier with a 0-3.3V analog video signal or a 3.3V logic level
  signal for blanking. Note that the default state has the beam OFF, so
  you will either need to connect the video in pin to 3.3V or adjust the
  brightness pot to see anything on the screen.

3. Video Amplifier Bias Supply
  The deflection board needs a stiff 60V bias supply for the video
  amplifier. This board provides it given a 12V input. With some
  modifications you could use this board as a Nixie tube power supply.
  For that you would need to change the value of R1 and C5 (to have the
  proper voltage rating).


