# SolarBridge
An ESP8266 Based bridge between GroWatt Solar API, Toon, Pulses and webinterface


A very cheap to built software bridge which can be installed on a Wemos mini (Aliexpress ab. 2 euros) and a PC817 optocoupler (Aliexpress ab. 10 cents). In this case it is not needed to install a power meter into the fuse box. Also it is possible to easily connect the GroWatt converter to the Toon, even if the inverter is located far arway from the meter adapter.

![Image 1](https://github.com/oepi-loepi/SolarBridge/blob/Images/Images/IMG_0515.jpg)

It will check solarpower from the GroWatt API every 1 minute. It will convert the Solarpower to S0 pulses (divided over the minute) and it will serve a webpage.


1. Built it
2. Upload the software
3. Use the AutoConnectAP to install the wifi and the GroWatt credentals (same as used for the webpage or app)
4. Find the DHCP web adres or the static web adres and goto the web page
5. Connect the Wemos to the meteradapter

Solar Bridge for GroWatt solar converters
This bridge will get the data from the GroWatt web interface (API) and create S0 pulses and led flashes
Each pulse/flash will suggest 1 Watt

![Image 5](https://github.com/oepi-loepi/SolarBridge/blob/Images/Images/IMG_0523.jpg)

On GPIO 4 a resistor (330 ohm and red LED are connected in series
PIN D2 ---- Resistor 33Ohm) ---- (Long LED lead ---- LED ---- Short LED Lead) ----- GND

On GPIO 5 a PC817 optocoupler is connected
PIN D1 ---- PC817 (anode, pin 1, spot)
GND ------- PC817 (cathode, pin 2)

Pin 3 and 4 of the PC817 will be a potential free contact

![Image 3](https://github.com/oepi-loepi/SolarBridge/blob/Images/Images/IMG_0516.jpg)
![Image 4](https://github.com/oepi-loepi/SolarBridge/blob/Images/Images/IMG_0519.jpg)


After uploading the sketch to the Wemos D1 mini, connect to the AutoConnectAP wifi.
Goto 192.168.4.1 in a webbrowser and fill in all data including GroWatt credentials.
