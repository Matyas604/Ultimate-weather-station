# Ultimate weather station
For a long time, I’ve wanted to know the current temperature, humidity, air quality, and more outside. Since weather forecasts are never accurate for my exact location, I wanted to know what the conditions really are. So, since I already have a lot of experience, I decided to build a complete weather station that would measure the values I wanted, based exactly on the sensors I chose. And since I have a [Home Assistant](https://www.home-assistant.io/) at home, I could make the station smart and monitor the data from anywhere.

This project was more about 3D modeling than PCB design, but in the end, I’m very satisfied.

## Features
- **Contains sensors:** [SHT45](https://sensirion.com/media/documents/33FD6951/67EB9032/HT_DS_Datasheet_SHT4x_5.pdf), [BMP280](https://www.bosch-sensortec.com/media/boschsensortec/downloads/datasheets/bst-bmp280-ds001.pdf), [SGP41](https://sensirion.com/media/documents/5FE8673C/61E96F50/Sensirion_Gas_Sensors_Datasheet_SGP41.pdf), and the [AS3935](https://cdn.sparkfun.com/assets/learn_tutorials/9/2/1/AS3935_Datasheet_EN_v2.pdf) and [LM393](https://www.onsemi.com/download/data-sheet/pdf/lm393-d.pdf) integrated circuits  
- **It can measure:** [temperature](https://en.wikipedia.org/wiki/Temperature), [humidity](https://en.wikipedia.org/wiki/Humidity), [pressure](https://en.wikipedia.org/wiki/Atmospheric_pressure), [air quality](https://en.wikipedia.org/wiki/Air_quality_index), [lightning distance and energy](https://en.wikipedia.org/wiki/Lightning), [wind speed](https://en.wikipedia.org/wiki/Wind_speed) and whether it is raining
- It's connected to [Home Assistant](https://www.home-assistant.io/), so I can use the data to set up automations and monitor the readings even when I'm not at home
- The [ESP32-S3](https://documentation.espressif.com/esp32-s3_datasheet_en.pdf) is the brain of the entire station
- It has two PCBs, one main board and another with sensors located inside the [radiation shield](https://en.wikipedia.org/wiki/Stevenson_screen) that measure the readings. They are connected to each other with a 7-wire cable

## CAD model
It includes a box for the main board and a radiation shield, which is secured with M5 rods and nuts, on top is an anemometer propeller for measuring wind speed. I’ll be placing the weather station on the balcony, so I’ve made a mount for it. It will be attached to the railing, which has a 14° slope, so the mount is designed to keep the radiation shield straight. The shield is connected to the mount with an M6 rod and M6 nuts, there is also a mount for the rain sensor. The railing mount is secured with two parts connected by M6 bolts and nuts.
<p align="center">
  <img src="Assets/Radiation shield CAD.png" alt="Radiation shield CAD" width="500">
</p>
<p align="center">
  <img src="Assets/Main case CAD.png" alt="Main case CAD" width="500">
</p>
<p align="center">
  <strong>Made in Fusion360</strong>
</p>

## PCBs
### Main PCB:
<p align="center">
  Schematic
</p>
<p align="center">
  <img src="Assets/Main PCB schematic.png" alt="Main PCB schematic" width="600">
</p>
<p align="center">
  PCB
</p>
<p align="center">
  <img src="Assets/Main PCB.png" alt="Main PCB" width="800">
</p>

### Sensors PCB:
<p align="center">
  Schematic
</p>
<p align="center">
  <img src="Assets/Sensors PCB schematic.png" alt="Sensors PCB schematic" width="900">
</p>
<p align="center">
  PCB
</p>
<p align="center">
  <img src="Assets/Sensors PCB.png" alt="Sensors PCB" width="1000">
</p>
<p align="center">
  <strong>Made in KiCad</strong>
</p>

## Firmware
This weather station uses [ESPHome](https://esphome.io/) firmware. It is programmed via the USB-C port on the main board. Thanks to ESPHome, it connects to [Home Assistant](https://www.home-assistant.io/), where I can then create various automations and view data from anywhere.

<hr>

<p align="center">
  Made with ❤️ by <a href="https://github.com/Matyas604">@Matyas604</a>
</p>
