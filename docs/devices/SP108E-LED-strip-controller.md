This is a controller for the WS2812 and similar LED chips (stripes). Prize is 13..15€ at ebay.
It uses another controller (STM32F0) to control CLK and Data lines to the LED stripes.

Warning: Construction zone. To run Tasmota on it, we need to modify the hardware. See [**here**](/docs/devices/SP108E-HardwareMod) and [**here**](/docs/devices/SP108E-HardwareAnalysis) for details.

If you don't need the CLK line you should use the controller [SP501E](https://templates.blakadder.com/SP501E.html) instead.

There are at least two versions of SP108e:

## SP108E
![sp108e](https://user-images.githubusercontent.com/19874899/46249748-c2c48980-c42e-11e8-9b35-2cbfc38d2fb9.jpg)

## SP108E v2 with ESP8285
![sp108ev2](https://ibb.co/ssTH70H"><img src="https://i.ibb.co/JrYQZfQ/sp108ev2.png)
