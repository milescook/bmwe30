# Speeduino ECU pins
This is a list of speedunio pins and on the other side of the connector <=> which ECU output and wire colour they corespond to. Most keep the original pin numbers but not all.



## Pin no, Function -> (IDC ribbon number) <=> harness wire # & colour
* Pin number corresponds to the speeduno IDC pin number
* IDC ribbon number is what is labelled (see table after this) as IDC numbering is different to speeduino pin numbers
* Harness wire is where it comes out of the ECU connector

* 1	Injector 1 - Pin 1/2 -> *Injector 1&6* (40) <=> 1 Yellow
* 2	Injector 2 - Pin 1/2 -> *Injector 2&5* (38) <=> 2 Blue
* 3	Injector 3 - Pin 1/2 -> *Injector 3&4* (36) <=> 3 Green
* 4	Injector 3 - Pin 2/2 -> *Injector 3&4* (34) <=> 4 White
* 5	Injector 4 - Pin 1/2 - Unused
* 6	Injector 4 - Pin 2/2 - Unused
* 7	Ignition 1 -> *Coil on plug 1 & 6* (28) <=> 7 Yellow
* 8	Ignition 4 -> *Unused*
* 9	Ground -> (26) <=> 8 Blue
* 10	Ground
* 11	MAP Sensor (0v-5v) *N/A - using onboard sensor*
* 12	TPS Ground 
* 13	5v - TPS
* 14	Proto Area 1 (0.4.4b+ Flex Sensor)
* 15	Proto Area 2 (0.4.4b+ Fan)
* 16	Proto Area 3 (0.4.4b+ Fuel Pump) -> Fuel Pump Relay (10) <=> 16 Yellow
* 17	Proto Area 4 (0.4.4b+ Tachometer) -> AIM Dash Tacho (8) <=> 17 Blue
* 18	Proto Area 5 (0.4.4b+ Clutch)
* 19	Coolant (CLT) -> *Blue temp sender* (4) <=> 19 Green
* 20	Inlet Air Temp (IAT) -> *New IAT Sensor* (2) <=> 20 White
* 21	O2 Sensor -> *Exhaust Lambda Sensor* (1) <=> 21 Blue
* 22	TPS input -> *Variable Auto BMW TPS* (3) <=> 22 Black
* 23	Ground -> Crank ground (5) <=> 23 shielded
* 24	Cam Input / VR2+
* 25	Crank Input / VR1+ (9) <=> 25 shielded
* 26	VR2- (Not used for hall sensor)
* 27	VR1- (Not used for hall sensor)
* 28	5v
* 29	Idle Stepper 2B
* 30	Idle Stepper 2A
* 31	Idle Stepper 1A
* 32	Idle Stepper 1B
* 33	Ignition 3 -> *Coil on plug 3 & 4* (25) <=> Green
* 34	Ignition 2 -> *Coil on plug 2 & 5* (27) <=> White
* 35	Boost *N/A No snail for us, yet....*
* 36	Idle 2 (For use with 3 wire idle valves)
* 37	PWM Idle
* 38	VVT
* 39	Injector 2 - Pin 2/2 -> *Injector 2&5* (32) <=> 5 Red
* 40	Injector 1 - Pin 2/2 -> *Injector 1&6* (30) <=> 6 Black


## Fun fact - 40 pin IDC wire numbers don't correspond to speeduino numbers...

### IDC Ribbon number, Speeduino IDC pin number
* 40 <=> 1
* 39 <=> 40
* 38 <=> 2
* 37 <=> 39
* 36 <=> 3
* 35 <=> 38
* 34 <=> 4
* 33 <=> 37
* 32 <=> 5
* 31 <=> 36
* 30 <=> 6
* 29 <=> 35
* 28 <=> 7
* 27 <=> 34
* 26 <=> 8
* 25 <=> 33
* 24 <=> 9
* 23 <=> 32
* 22 <=> 10
* 21 <=> 31
* 20 <=> 11
* 19 <=> 30
* 18 <=> 12
* 17 <=> 29
* 16 <=> 13
* 15 <=> 28
* 14 <=> 14
* 13 <=> 27
* 12 <=> 15
* 11 <=> 26
* 10 <=> 16
* 9 <=> 25
* 8 <=> 17
* 7 <=> 24
* 6 <=> 18
* 5 <=> 23
* 4 <=> 19
* 3 <=> 22
* 2 <=> 20
* 1 <=> 21

