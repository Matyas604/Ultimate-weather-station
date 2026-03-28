# Ultimate weather station
For a long time, I’ve wanted to know the current temperature, humidity, air quality, and more outside. Since weather forecasts are never accurate for my exact location, I wanted to know what the conditions really are. So, since I already have a lot of experience, I decided to build a complete weather station that would measure the values I wanted, based exactly on the sensors I chose. And since I have a [Home Assistant](https://www.home-assistant.io/) at home, I could make the station smart and monitor the data from anywhere.

This project was more about 3D modeling than PCB design, but in the end, I’m very satisfied.

## Features
- **Contains sensors:** [SHT45](https://sensirion.com/media/documents/33FD6951/67EB9032/HT_DS_Datasheet_SHT4x_5.pdf), [BMP280](https://www.bosch-sensortec.com/media/boschsensortec/downloads/datasheets/bst-bmp280-ds001.pdf), [SGP41](https://sensirion.com/media/documents/5FE8673C/61E96F50/Sensirion_Gas_Sensors_Datasheet_SGP41.pdf), and the [AS3935](https://cdn.sparkfun.com/assets/learn_tutorials/9/2/1/AS3935_Datasheet_EN_v2.pdf) and [LM393](https://www.onsemi.com/download/data-sheet/pdf/lm393-d.pdf) integrated circuits  
- **It can measure:** [temperature](https://en.wikipedia.org/wiki/Temperature), [humidity](https://en.wikipedia.org/wiki/Humidity), [pressure](https://en.wikipedia.org/wiki/Atmospheric_pressure), [air quality](https://en.wikipedia.org/wiki/Air_quality_index), [lightning distance and energy](https://en.wikipedia.org/wiki/Lightning), and whether it is raining
- It's connected to [Home Assistant](https://www.home-assistant.io/), so I can use the data to set up automations and monitor the readings even when I'm not at home
- The [ESP32-S3](https://documentation.espressif.com/esp32-s3_datasheet_en.pdf) is the brain of the entire station
- It has two PCBs, one main board and another with sensors located inside the [radiation shield](https://en.wikipedia.org/wiki/Stevenson_screen) that measure the readings. They are connected to each other with a 7-wire cable
