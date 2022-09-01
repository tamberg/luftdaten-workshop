# Luftdaten Workshop
Initiiert von [Smart City Zürich](https://stadt-zuerich.ch/smart-city), mit [@tamberg](https://twitter.com/tamberg) und [@twulls](https://twitter.com/twulls) vom [IMVS](https://www.fhnw.ch/de/die-fhnw/hochschulen/ht/institute/institut-fuer-mobile-und-verteilte-systeme), [FHNW](https://www.fhnw.ch/).

Verwendet Source Code von [Open Data Stuttgart](https://github.com/opendata-stuttgart), lizenziert unter [GPLv3](https://github.com/opendata-stuttgart/sensors-software/blob/master/airrohr-firmware/airrohr-firmware.ino#L8-L23).

Publiziert Daten auf die [Sensor.Community](https://sensor.community/de/) Plattform unter [DbCL v1.0](https://opendatacommons.org/licenses/dbcl/1-0/).

<img src="https://live.staticflickr.com/65535/52190850590_b975aff403_o.gif"/>

## Material auspacken und prüfen
Das Luftdaten Kit sollte die folgenden Teile enthalten:

<img src="https://live.staticflickr.com/65535/52190368383_59d8d941df_b.jpg"/>

* 2 * Rohr, grau
* 2 * Netz, blau
* 3 * Kabelbinder, gross
* 3 * Kabelbinder, klein
* 7 * F-F Jumper Kabel, farbig (bzw. 3 + 4)
* 1 * Micro USB Kabel, lang
* 1 * 230V USB Adapter
* 1 * Schlauch, 20 cm
* 1 * SDS011 Feinstaub Sensor, silber, schwarz*
* 1 * ESP8266 NodeMCU Mikrocontroller, schwarz
* 1 * DHT22 Temperatur- und Feuchtigkeitssensor, rot**

<sup>*</sup>Das dicke, weisse Kabel im selben Paket braucht's nicht.<br/>
<sup>**</sup>In manchen Kits ist der DHT22 Sensor ohne den roten Teil.

### ESP8266 NodeMCU Mikrocontroller
Dieser Mikrocontroller ist ein kleiner Computer mit Wi-Fi.

Die goldene, eckige Linie oben ist seine Wi-Fi Antenne.

Über die Pins an den Seiten kann er Sensoren auslesen.

<img src="https://live.staticflickr.com/65535/52190288098_0949c03e22_b.jpg" width="480"/>

### SDS011 Feinstaub Sensor
Dieser Sensor kann Feinstaub Partikel messen, ein Mass für die Luftqualität.

### DHT22 Sensor
Dieser Sensor kann die Temperatur und die Feuchtigkeit der Luft messen.

## Sensor und Gehäuse bauen
> Achtung: Den Strom bzw. USB schliessen wir erst ganz am Schluss an, wenn alles fertig ist.

### Kabel an ESP8266 NodeMCU Mikrocontroller anstecken
Die Farben der Kabel und die genaue Position sind wichtig.

<img src="https://live.staticflickr.com/65535/52190287993_e04a10e5da_b.jpg" width="540"/>

Der Alu Teil oben auf dem ESP8266 NodeMCU hilft bei der Orientierung.

<img src="https://live.staticflickr.com/65535/52190528124_6aa5e9a2c6_b.jpg" width="540"/>

### SDS011 Feinstaub Sensor an 4-er Kabel anstecken
<img src="" width="540"/>

### DHT22 Sensor an 3-er Kabel anstecken
Die rote Variante hat drei Anschlüsse:

<img src="https://live.staticflickr.com/65535/52189260537_c8973c89ae_b.jpg" width="480"/>

Die andere Variante hat vier, ein Platz bleibt leer:

<img src="https://live.staticflickr.com/65535/52321570598_684f144f31_b.jpg" width="480"/>

### Zwischenstand: Elektronik komplett
<img src="" width="540"/>

### Schlauch an Feinstaub Sensor stecken

### Elektronik ins Rohr stecken
<img src="" width="540"/>

### Rohr zusammenstecken
<img src="" width="540"/>

Details siehe https://github.com/opendata-stuttgart/meta/blob/master/flyer/assemble_station.150dpi.pdf

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

## Sensor Community Forum
https://forum.sensor.community/
