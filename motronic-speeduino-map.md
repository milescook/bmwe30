# How to map standard motronic 1.3 harness to speeduino pins (Work in progress)

See https://wiki.speeduino.com/en/boards/V04 for Speeduino pins.



For the Motronic pins see  https://www.e30zone.net/e30wiki/index.php?title=ECU_Pinouts#Motronic_1.3


For comparison, see the megasquirt map here For the megasquirt map see https://www.e30zone.net/e30wiki/index.php?title=Megasquirting_Your_M20


# Pin assignments

- Motronic pin  - Description - Speeduino Pin - Speeduino description - Purpose
- 1 - Ignition Coil Output (Channel 1 - 1.1) - 7 | Ignition 1 
- 2 - Ground - 9 - Ground
- 3 - Fuel Pump Relay Control - 16 - Proto Area 3 (0.4.4b+ Fuel Pump)
- 4 - Idle out - 37 - PWM Idle
- 5 - NA
- 6 - Tachometer output - 17 - Proto Area 4 (0.4.4b+ Tachometer) 
- 7 - External Map Signal In - NA
- 8 - Cam Hall Sensor Signal In - NA
- 10 - Oxygen sensor (ground) - 10 - Ground
- 22 - Idle out - 36 - PWM Idle 2
- 28 - O2 input - 21 - O2 Sensor


# Other motroinic pins

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

