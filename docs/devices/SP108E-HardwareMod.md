Warning: Construction zone.

## SP108Ev1
Below is correct, but IO0 is directly connected to VCC, so we cannot bring ESP-12 into flash mode. Will check for some OTA mode that can be used.

With just two additional wires we can use Tasmota with the SP108E.

[**Analysis of the hardware**](/devices/SP108E-HardwareAnalysis)

The trick is to hold the STM32F0 controller in reset. Then we do not need to cut any traces on the PCB because all pins of the STM32F0 are inputs.

Another warning: I did not yet proof it actually works, this is work in progress.

- Wire 1 - NRST (pin 7) of STM32F0 to GND
- Wire 2 - IO4 of ESP-12 to R4


![pins svg](https://user-images.githubusercontent.com/19874899/46259105-0a9dec00-c4d5-11e8-9874-d0f72e7a6934.png)

## SP108Ev2
![sp108ev2-inside](https://i.ibb.co/XVmNZQ5/sp108ev2-inside.png)

Wiring:
- Reset Pin of STM32F0 to GND like described above for v1
- GPIO0 to Reset Button for Flashing
- GPIO2 to LED Data line
- GPIO13 to LED Clock line
- temporary: TX/RX to usb serial flash tool

Additional you could connect the LEDs to the remaining GPIOs.

After that, hold down Reset button on powerup and flash Tasmota
