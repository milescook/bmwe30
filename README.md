# bmwe30
Assortment of docs and diagrams for the race car

# Shopping list
## ECU Wiring
* 40pin connectorribbon - https://thepihut.com/products/raspberry-pi-40-pin-gpio-socket-connector-to-labelled-pins-female-150mm
* Standard ecu connectors - https://www.ebay.co.uk/itm/334459759696

## Sensors
See https://wiki.speeduino.com/en/wiring/system
* Wideband lambda controller and sensor - https://diy-efi.co.uk/product/14point7-spartan2-wideband
* (Variable TPS is in the garage somewhere...)
* IAT - https://diy-efi.co.uk/product/m12-iat-sensor
* Coolant temp sensor - will use existing blue sender
* Idle control valve - Can I use existing???? PWM or stepper...?????


# Speeduino ECU pins
This is a list of speedunio pins and on the other side of the connector <=> which ECU output and wire colour they corespond to. Most keep the original pin numbers but not all.

## Pin #,Function, <=> ECU connector pin, ECU harness wire colour
* 1	Injector 1 - Pin 1/2 -> *Injector 1* <=> 1 Yellow
* 2	Injector 2 - Pin 1/2 -> *Injector 4* <=> 2 Blue
* 3	Injector 3 - Pin 1/2 -> *Injector 2* <=> 3 Green
* 4	Injector 3 - Pin 2/2 -> *Injector 6* <=> 4 White
* 5	Injector 4 - Pin 1/2 - Unused
* 6	Injector 4 - Pin 2/2 - Unused
* 7	Ignition 1 -> *Coil on plug 1 & 2* <=> 7 Yellow
* 8	Ignition 4 -> *Unused*
* 9	Ground <=> 8 Blue
* 10	Ground
* 11	MAP Sensor (0v-5v) *N/A - using onboard sensor*
* 12	Ground 
* 13	5v <=> 13 Red
* 14	Proto Area 1 (0.4.4b+ Flex Sensor)
* 15	Proto Area 2 (0.4.4b+ Fan)
* 16	Proto Area 3 (0.4.4b+ Fuel Pump)
* 17	Proto Area 4 (0.4.4b+ Tachometer)
* 18	Proto Area 5 (0.4.4b+ Clutch)
* 19	Coolant (CLT) -> *Blue temp sender*
* 20	Inlet Air Temp (IAT) -> *New IAT Sensor*
* 21	O2 Sensor -> *Exhaust Lambda Sensor*
* 22	TPS input -> *Variable Auto BMW TPS*
* 23	Ground
* 24	Cam Input / VR2+
* 25	Crank Input / VR1+
* 26	VR2- (Not used for hall sensor)
* 27	VR1- (Not used for hall sensor)
* 28	5v
* 29	Idle Stepper 2B
* 30	Idle Stepper 2A
* 31	Idle Stepper 1A
* 32	Idle Stepper 1B
* 33	Ignition 3 -> *Coil on plug 5 & 6*
* 34	Ignition 2 -> *Coil on plug 3 & 4*
* 35	Boost *N/A No snail for us, yet....*
* 36	Idle 2 (For use with 3 wire idle valves)
* 37	PWM Idle
* 38	VVT
* 39	Injector 2 - Pin 2/2 -> *Injector 3* <=> 5 Red
* 40	Injector 1 - Pin 2/2 -> *Injector 5* <=> 6 Black
