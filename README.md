Description
===========

The MeteoBox (MeteoKutija) is a cheap device that collects a set of meteorological
data and publishes it to a central database. We will use cheap of-the-shelf hardware,
such as sensors, micro-controllers and embedded linux devices so that the device would be
available to anyone with the will and some patience.

The device is based on a OpenWrt compatible embedded linux device (typically a common WiFi router),
and a single AVR micro-controller (attiny2313 or atmega328) for communication with the sensors.

The router needs to have a USART port (easily hacked on TP-Link routers) to communicate with the
AVR micro-controller. We will use the CmdMessenger protocol for this communication.

The AVR micro-controller will then communicate with the sensors, either through I²C or 1-Wire
protocols. For sensors that don't implement I²C or 1-Wire we'll use a Attiny25 controller to
handle the communication.

Once data is gathered on the router it's published to a central database (CouchDB + spatial).
Since the database will be open to the public, anyone could make web apps to display the data
in a interesting way.


References
==========

* https://en.wikipedia.org/wiki/1-Wire
* https://en.wikipedia.org/wiki/I2c
* http://arduino.cc/playground/Code/CmdMessenger (https://github.com/dreamcat4/CmdMessenger)
* http://wiki.openwrt.org/toh/tp-link/tl-mr3420
* http://rcouch.org/docs/
