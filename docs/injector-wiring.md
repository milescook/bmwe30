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


# Injector subloom
You can't use the existing E30 M20 injector wiring, because Motronic 1.3 firs in 2 batches of 3. Speeduino doesn't support this, and has 4 injector channels so you have to run it in paired mode, 3 pairs of 2. So instead of re-wiring the injector loom I bought this excellent depin tool (the service was fantastic) from https://falkmfg.com/products/depin-tool and made a replacement.