# Overview

The objective here is a ts-dash (see http://tunerstudio.com/index.php/products/ts-dash) replacement for the instrument clocks, using the standard E30 wiring.

![Dash](ts-dash.png)

## Pins

https://www.e30zone.net/e30wiki/images/b/b2/Instrument_Cluster.pdf

## C1 (Blue)
26 Pins

- 7 Tachometer (now Speeduino USB serial date TX from Motronic pin 6) to Pi 10 RX - Orange
- 11 Fuel flow rate (now Speeduino USB serial date RX from Motronic pin 32) to Pi 8 TX - Yellow
- 14 Alternator light +
- 16 Alternator lights -
- 18 Oil  
- 20 GND
- 23 Live 12v

# Diagrams
![Plug](dash-blue-port-pins.png)
![Plug](dash-blue-plug-pins.png)

## C2 (White)
26 Pins

- 4 Left fuel tank sender gnd
- 5 Fuel tank sender gnd
- 8 Speed sensor
- 13 Speed sensor