# How to map standard motronic 1.3 harness to speeduino pins (Work in progress)

WARNING: This is my wiring map, and WILL NOT work for you without harness modification. I'm re-purposing some of the ECU pins for a start, and changing the injector sub loom completely (from 2 batched to 6 individual but running as 3 pairs). I'm trying to use as much of the ECU connector as possible without changing the wiring where I can. For ignition timing I'll need a new loom anyway, as M20s used a single ignition coil and distrubtor running off the cam. I'll keep this initially for simplicity.

See https://wiki.speeduino.com/en/boards/V04 for Speeduino pins.


For the Motronic pins see  https://www.e30zone.net/e30wiki/index.php?title=ECU_Pinouts#Motronic_1.3


For comparison, see the megasquirt map here for the Megasquirt map see https://www.e30zone.net/e30wiki/index.php?title=Megasquirting_Your_M20


# Pin assignments

So you see here the map for my Motronic 1.3 harness ECU pin, to Speeduino pin, followed lastly by IDC pin. IDC is the dupont ribbon connector https://thepihut.com/products/raspberry-pi-40-pin-gpio-socket-connector-to-labelled-pins-female-150mm I have going to the Speeduino which handily labels all it's wires. Took me a while to realise that the numbers labelled have no correlation to the speeduino pins... ah well. I did make a handy map [idc-numberedpins.md](idc-numberedpins.md)

- Motronic pin  - Description - Speeduino Pin - Speeduino description - {Purpose} - IDC Pin
- 1 - Ignition Coil Output (Channel 1 - 1.1) - 7 | Ignition 1 
- 2 - Ground - N/A - ECU Power relay ground, pin 30
- 3 - Fuel Pump Relay Control - 38 - Boost control (swap from 16 fuel pump as I have no ULN chip) - 35
- 4 - Idle out - 37 - PWM Idle - 33
- 5 - NA
- 6 - Tachometer output - 17 - Proto Area 4 (0.4.4b+ Tachometer) 
- 7 - AFM input pin 2 - 19 - Coolant (CLT) - 4
- 10 - Oxygen sensor (ground) - 10 - Ground - 22
- 14 - Injector gnd (???) - 12 - Ground - 18
- 16 - Injectors 1,3,5 - 2 - Injector 2 Pin 1/2 - Injector 2 - 38
- 16 - Injectors 1,3,5 - 39 - Injector 2 Pin 2/2 - Injector 5 - 37
- 17 - Injectors 2,4,6 - 3 - Injector 3 Pin 1/2 - Injector 3 - 36
- 17 - Injectors 2,4,6 - 4 - Injector 3 Pin 2/2 - Injector 4 - 34
- 19 - Main gound - ECU Power relay 85 & speeduino power -ve
- 22 - Idle out - 36 - PWM Idle 2 - 31
- 26 - AFM Common ground - 9 - Ground - IAT  / CLT Ground  - 24
- 27 - Start input- to ignition switch and coil - N/A - ECU Power relay pin 86
- 28 - O2 input - 21 - O2 Sensor - 1
- 36 - Main relay output - N/A - ECU Power relay pin 87
- 37 - Switched power from main relay - NA - Speeduino power +ve in - NA
- 44 - AFM air inlet temp pin 1 - 20 - Inlet Air Temp (IAT) - 2
- 45 - Coolant Temp input - 1 - Injector 1 Pin 1/2 - Injector 1 - 40
- 45 - Coolant Temp input - 40 - Injector 1 Pin 2/2 - Injector 6 - 39
- 47 - CPS Signal - 25 - Crank Input / VR1+ - 9
- 48 - CPS gnd - 27 VR1- - 13
- 52 - Closed throttle - 22 - TPS Input - 3
- 53 - WOT Input - 13 - 5V (TPS Live) - 16

# AFM Plug re-purpose
- Pin no - ECU Pin No - New purpose - Speeduino pin
- 1 - 44 - Inlet Air Temp (IAT) - 20
- 2 - 7 - Coolant (CLT) - 19
- 3 - 12 - Unused
- 4 - 26 - IAT / CLT Ground - 9

# TPS

E36 TPS Pin - E30 Pin - Purpose - Motronic pin - Speeduino Pin - IDC Pin
- 1 - 2 - GND - N/A
- 2 - 1 - Signal - 52 - 22 - 3
- 3 - 3 - Vref (5v) 53 - 13 - 16

# Other motronic pins

- 18 - Constant 12V from Battery - 12v positive (temporary power but will become unused)
- 19 - Main ground - 12v negative
- 27 - Start input - Goes to the main power relay in the new ECU case
- 36 - Main relay ground
- 37 - Speeduino power


# ECU Relays

There is a relay for the speeduino (nothing special just Halfords).

## ECU Power relay 

See https://www.r3vlimited.com/board/forum/e30-technical-forums/engine-drivetrain/m20/338232-m20b25-fuel-pump-wiring
When 12v comes from pin 27, a new relay needs to ground pin 36. This will activate the main relay switching on power to pin 37, powering up the Speeduino

- ECU Pin - Relay pin - Destination / Description
- 27 - 86 - Ignition on 12v
- 19 - 85 - Motronic 19 (main gnd)
- 36 - 87
- 2 - 30 - Motronic 2 (gnd)



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

# Injectors connector
- Speeduino pin - Speeduino pin description - Description - ECU Pin
- 1 - Injector 1 - Pin 1/2 - Injector 1 - 45
- 2 - Injector 2 - Pin 1/2 - Injector 2 - 16
- 3 - Injector 3 - Pin 1/2 - Injector 3 - 17
- 4 - Injector 3 - Pin 2/2 - Injector 4 - 17
- 39 - Injector 2 - Pin 2/2 - Injector 5 - 16
- 40 - Injector 1 - Pin 2/2 - Injector 6 - 45


# New injector subloom C191 plug

![C191 Plug diagram from E30 Zone](https://www.e30zone.net/e30wiki/images/6/60/C191.jpg)

- C191 plug pin no | ECU Pin | description
- 1 - 45 - Fuel Injectors 1 & 6
- 2 - Unused Gnd
- 3 - Unused Gnd
- 4 - Unused goes to clocks
- 5 - NA - DME relay (live for Fuel Injectors)
- 6 - 16 - Fuel Injectors 2 & 5
- 7 - 17 - Fuel Injectors 3 & 4


# FOR REFERENCE: Original injector subloom wiring C191 plug

- C191 plug pin no | ECU Pin | description
- 1 - 45 - Coolant Temperature Sensor
- 2 - NA - Coolant Temperature Sensor
- 3 - NA - Coolant Temperature Sensor
- 4 - NA - Coolant Temperature Sensor
- 5 - NA - DME relay (live for Fuel Injectors)
- 6 - 16 - Fuel Injectors 1, 3, 5
- 7 - 17 - Fuel Injectors 2, 4, 6



