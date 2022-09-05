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
Der ESP8266 Mikrocontroller ist ein kleiner Computer mit Internet Verbindung.

Die goldene, eckige Linie am oberen Rand ist seine Wi-Fi Antenne.

Über die Pins an den Seiten kann er Sensoren auslesen.

<img src="https://live.staticflickr.com/65535/52335798266_52f71578d8_b.jpg" width="480"/>

### SDS011 Feinstaub Sensor
Dieser Sensor kann Feinstaub Partikel messen, ein Mass für die Luftqualität.

<img src="https://live.staticflickr.com/65535/52336094894_03777b0b4f_b.jpg" width="480"/>

### DHT22 Sensor
Dieser Sensor kann die Temperatur und die Feuchtigkeit der Luft messen.

## Sensor und Gehäuse bauen
> Achtung: Den Strom bzw. USB erst anschliessen, wenn die Elektronik fertig verkabelt ist.

### Kabel an ESP8266 NodeMCU Mikrocontroller anstecken
Die Farben der Kabel und die genaue Position sind wichtig.

G = schwarz, VU = weiss

<img src="https://live.staticflickr.com/65535/52190287993_e04a10e5da_b.jpg" width="540"/>

Der Alu Teil oben auf dem ESP8266 NodeMCU hilft bei der Orientierung.

D7 = orange, G = braun, 3V = rot, D2 = grau, D1 = violett

<img src="https://live.staticflickr.com/65535/52190528124_6aa5e9a2c6_b.jpg" width="540"/>

### SDS011 Feinstaub Sensor an 4-er Kabel anstecken
TXD = violett, RXD = grau, GND = schwarz, (leer), 5V = weiss, (leer), (leer)

<img src="https://live.staticflickr.com/65535/52190756335_3807218db2_b.jpg" width="540"/>

### DHT22 Sensor an 3-er Kabel anstecken (Variante rot)
> Achtung: Nur für die rote Variante, sonst geht's [hier weiter](#dht22-sensor-an-3-er-kabel-anstecken-variante-weiss).

Diese Variante des Sensors hat drei Pins für Kabel:

GND = braun, VCC = rot, DAT = orange

<img src="https://live.staticflickr.com/65535/52189260537_c8973c89ae_b.jpg" width="480"/>

### DHT22 Sensor an 3-er Kabel anstecken (Variante weiss)

Diese Variante des Sensors hat vier Pins, ein Pin bleibt leer:

VCC = rot, DAT = orange, (leer), GND = braun

<img src="https://live.staticflickr.com/65535/52321570598_e6090ed620_b.jpg" width="480"/>

Ein Stück Tape hilft, die Kabel zu fixieren - auf der Rückseite:

<img src="https://live.staticflickr.com/65535/52320457907_4fcb69f0cb_b.jpg" width="480"/>

### Zwischenstand: Elektronik komplett
<img src="https://live.staticflickr.com/65535/52189260562_b2812e12cd_b.jpg" width="480"/>

Es ist gut, vor dem Einbau der Elektronik ins Rohr, alles zu testen.

Dazu braucht es die folgenden Schritte:

* [Sensor Firmware flashen](#sensor-firmware-flashen) (falls keine Sensor ID auf dem Kit steht)
* [Sensor Wi-Fi konfigurieren](#Sensor-wi-fi-konfigurieren) (für das Wi-Fi Netzwerk im Workshop)
* [Sensor bei Community registrieren](#sensor-bei-community-registrieren) (um eigene Daten zu finden)

### Schlauch an Feinstaub Sensor stecken
<img src="" width="540"/>

### Elektronik ins Rohr stecken
<img src="" width="540"/>

### Rohr zusammenstecken
<img src="" width="540"/>

### Fertiger Sensor

Nun ist der Luftdaten Sensor bereit zur Montage, z.B. auf dem Balkon.

Der folgende Schritt muss zu Hause nochmal durchgeführt werden:

* [Sensor Wi-Fi konfigurieren](#) (für das Wi-Fi Netzwerk zu Hause)

## Sensor Firmware flashen
> Achtung: Für den Workshop wurde die Firmware bereits auf den ESP8266 NodeMCU Mikrocontroller geflasht.

Um den Sensor zu Programmieren, braucht es einen Computer mit Arduino Entwicklungsumgebung https://arduino.cc/

Zudem diesen USB Treiber https://www.silabs.com/developers/usb-to-uart-bridge-vcp-drivers (CP210x, für NodeMCU v2)

Und diesen Code https://github.com/opendata-stuttgart/sensors-software/blob/master/airrohr-firmware/airrohr-firmware.ino

Nach dem Flashen gibt der ESP8266 NodeMCU Mikrocontroller via USB eine Sensor ID aus, diese braucht es beim Registrieren.

## Sensor Wi-Fi konfigurieren
https://github.com/opendata-stuttgart/meta/wiki/Konfiguration-der-Sensoren
* AP ID: airRohr-12345678

Siehe auch https://github.com/opendata-stuttgart/meta/blob/master/flyer/assemble_station.150dpi.pdf

## Sensor bei Community registrieren
https://devices.sensor.community/sensors/register

## Sensor Community Karte mit Daten anzeigen
https://maps.sensor.community/#12/47.3775/8.5367

## Sensor Community Forum
https://forum.sensor.community/
