# ESP-pwm-4ch

ESP8266/ESP32 based board with 4x PWM output channels.

This board is designed to be driven by an Olimex ESP32-POE, ESP32-POE-ISO or Wemos D1 Mini modules running Tasmota. If you want to use the ethernet interface present on the Olimex modules you will need to compile your own Tasmota binaries enabling the corresponding features.

The design considers that the board will be mounted on a PCB DIN rail holder offered by the Brazilian manufacturer Metaltex. Check [here](https://www.metaltex.com.br/produtos/componentes/suportes/sp7-suporte-para-montagem-de-placa-de-circuito-impresso-em-trilho-din) for details.

Heatsinks are included in the design as I wasn't sure about how much power the MOSFETs would dissipate. The first tests were performed using zero ohm resistors between the drivers and the transistors. A 5A load was applied and the transistor showed no noticeable temperature elevation. In version 2 I replaced the zero ohm resistors for 22 ohm to avoid damages to the drivers, and this setup hasn't yet been tested. Given the very low switching frequency and small loads I suppose the heatsinks are still not needed.

Expect some flicker when driving LEDs with the ESP8266. It gets much more stable when using the hardware PWMs of the ESP32.

There is a preferred version of this board with 8x PWM channels and individual pins for powering groups of two outputs, what enables driving the full 5A per channel. Click [here](https://github.com/thermseekr/ESP-pwm-8ch) to check it.

![alt text](https://github.com/thermseekr/ESP-pwm-4ch/blob/main/V2/ESP-pwm-4ch-V2.png "ESP-pwm-4ch")
