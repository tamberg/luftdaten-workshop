# Luftdaten Workshop
Initiiert von [Smart City Zürich](https://stadt-zuerich.ch/smart-city), mit [@tamberg](https://twitter.com/tamberg) und [@twulls](https://twitter.com/twulls) vom [IMVS](https://www.fhnw.ch/de/die-fhnw/hochschulen/ht/institute/institut-fuer-mobile-und-verteilte-systeme), [FHNW](https://www.fhnw.ch/).

Verwendet Source Code von [Open Data Stuttgart](https://github.com/opendata-stuttgart), lizenziert unter [GPLv3](https://github.com/opendata-stuttgart/sensors-software/blob/master/airrohr-firmware/airrohr-firmware.ino#L8-L23).

Publiziert Daten auf die [Sensor.Community](https://sensor.community/de/) Plattform unter [DbCL v1.0](https://opendatacommons.org/licenses/dbcl/1-0/).

<img src="https://live.staticflickr.com/65535/52190850590_b975aff403_o.gif"/>

## Material auspacken und prüfen
<img src="https://live.staticflickr.com/65535/52190368383_59d8d941df_b.jpg"/>

* 2 * Rohr
* 2 * Netz
* 3 * Kabelbinder gross
* 3 * Kabelbinder klein
* 7 * F-F Jumper Kabel (bzw. 3 + 4)
* 1 * Micro USB Kabel
* 1 * 230V USB Adapter
* 1 * SDS011 Feinstaub Sensor
* 1 * ESP8266 NodeMCU Mikrocontroller
* 1 * DHT22 Temperatur & Feuchtigkeitssensor

## Sensor und Gehäuse bauen
https://github.com/opendata-stuttgart/meta/blob/master/flyer/assemble_station.150dpi.pdf
  * Ev. auch https://sensor.community/en/sensors/airrohr/
  * Und https://airbg.info/en/build-a-station/

## USB Treiber installieren (optional)
https://www.silabs.com/developers/usb-to-uart-bridge-vcp-drivers (CP210x, für NodeMCU v2)

## Arduino IDE installieren (optional)
https://arduino.cc/

## Sensor Firmware flashen
https://github.com/opendata-stuttgart/sensors-software/blob/master/airrohr-firmware/airrohr-firmware.ino
  * via https://github.com/opendata-stuttgart/sensors-software/tree/master/airrohr-firmware
  * via https://github.com/opendata-stuttgart/sensors-software
  * https://github.com/opendata-stuttgart/airrohr-firmware-flasher (?)

## Sensor Wi-Fi konfigurieren
https://github.com/opendata-stuttgart/meta/wiki/Konfiguration-der-Sensoren
  * AP ID: airRohr-12345678

## Sensor bei Community registrieren
https://devices.sensor.community/sensors/register

## Sensor Community Karte mit Daten azeigen
https://maps.sensor.community/#12/47.3775/8.5367

## Sensor Community Lizenzen für Firmware und Daten
* Firmware https://www.gnu.org/licenses/gpl-3.0.en.html
* Daten https://opendatacommons.org/licenses/dbcl/1-0/
* Fotos https://creativecommons.org/publicdomain/zero/1.0/deed.de

## Sensor Community Forum
https://forum.sensor.community/
