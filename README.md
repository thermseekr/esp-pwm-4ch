# ESP-PWM-4CH

ESP8266/ESP32 based board with 4x PWM output channels.

This board is designed to be driven by an Olimex ESP32-POE, ESP32-POE-ISO or Wemos D1 Mini modules.

The design considers that the board will be mounted on a PCB DIN rail holder offered by the Brazilian manufacturer Metaltex. Check [here](https://www.metaltex.com.br/produtos/componentes/suportes/sp7-suporte-para-montagem-de-placa-de-circuito-impresso-em-trilho-din) for details.

Heatsinks are included in the design as I wasn't sure about how much power the MOSFETs would dissipate. The first tests were performed using zero ohm resistors between the drivers and the transistors. A 5A load was applied and the transistor showed no noticeable temperature elevation. In version 2 I replaced the zero ohm resistors for 22 ohm to protect the drivers. Given the very low switching frequency and small loads I suppose the heatsinks are still not needed.

Expect some flicker when driving LEDs with the ESP8266. It gets much more stable when using the hardware PWMs of the ESP32.

There is a preferred version of this board with 8x PWM channels and individual pins for powering groups of two outputs, what enables driving the full 5A per channel. Click [here](https://github.com/thermseekr/esp-pwm-8ch) to check it.

![alt text](https://github.com/thermseekr/esp-pwm-4ch/blob/main/V2/esp-pwm-4ch-v2.png "ESP-PWM-4CH")
