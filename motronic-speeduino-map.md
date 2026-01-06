# How to map standard motronic 1.3 harness to speeduino pins (Work in progress)

WARNING: This is my wiring map, and WILL NOT work for you without harness modification. I'm re-purposing some of the ECU pins for a start, and changing the injector sub loom completely (from 2 batched to 6 individual but running ad 3 pairs). I'm trying to use as much of the ECU connector as possible without changing the wiring where I can. For ignition timing I'll need a new loom anyway, as M20s used a single ignition coil and distrubtor running off the cam. I'll keep this initially for simplicity.

See https://wiki.speeduino.com/en/boards/V04 for Speeduino pins.


For the Motronic pins see  https://www.e30zone.net/e30wiki/index.php?title=ECU_Pinouts#Motronic_1.3


For comparison, see the megasquirt map here for the Megasquirt map see https://www.e30zone.net/e30wiki/index.php?title=Megasquirting_Your_M20


# Pin assignments

- Motronic pin  - Description - Speeduino Pin - Speeduino description - Purpose - IDC Pin
- 1 - Ignition Coil Output (Channel 1 - 1.1) - 7 | Ignition 1 
- 2 - Ground - 9 - Ground
- 3 - Fuel Pump Relay Control - 16 - Proto Area 3 (0.4.4b+ Fuel Pump)
- 4 - Idle out - 37 - PWM Idle - 33
- 5 - NA
- 6 - Tachometer output - 17 - Proto Area 4 (0.4.4b+ Tachometer) 
- 7 - External Map Signal In - NA
- 8 - Cam Hall Sensor Signal In - NA
- 14 - GND (TPS) - 12 - Ground - TPS Ground - 18
- 10 - Oxygen sensor (ground) - 10 - Ground
- 22 - Idle out - 36 - PWM Idle 2 - 31
- 28 - O2 input - 21 - O2 Sensor
- 47 - CPS Signal - 25 - Crank Input / VR1+ - 9
- 48 - CPS gnd - 27 VR1- - 13
- 52 - Closed throttle - 22 - TPS Input - 3
- 53 - WOT Input - 13 - TPS Live - 16

# TPS

E36 TPS Pin - E30 Pin - Purpose - Motronic pin - Speeduino Pin - IDC Pin
- 1 - 2 - GND - 14 - 12 - 18
- 2 - 1 - Signal - 52 - 22 - 3
- 3 - 3 - Vref (5v) 53 - 13 - 16

# Other motronic pins

- 18 - Constant 12V from Battery - 12v positive
- 19 - Main ground - 12v negative

# Lambda
- Black - Signal - ECU Loom pin 28
- White - Heater - Fuel pump live relay
- Gray - Signal Ground - ECU Loom pin 10
- Gray - Heater Ground - ECU Loom ground

# Harness side to o2 side
- Green to white
- Brown to white
- black to gray
- yellow to black

# Injector connector
- Pin - Speeduino pin - Speeduino pin description - Description
- 1 - 1 - Injector 1 - Pin 1/2 - Injector 1
- 2 - 2 - Injector 2 - Pin 1/2 - Injector 2
- 3 - 3 - Injector 3 - Pin 1/2 - Injector 3
- 4 - 4 - Injector 3 - Pin 2/2 - Injector 4
- 5 - 39 - Injector 2 - Pin 2/2 - Injector 5
- 6 - 40 - Injector 1 - Pin 2/2 - Injector 6

