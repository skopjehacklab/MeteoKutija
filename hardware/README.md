Hadrware designs, kicad files

Power scheme:

The main router can deliver both 3v3 and 5v. The AVR controller will be powered from the 5v rail. There will be an LM1117-3v3 regulator on the sensor board for the I²C communication to the BMP085 sensor. There will be a logic shifter on the I²C line, composed of two BS170 NMOS FETs so that the 3v3 logic can be safely interfaced with the 5v logic. On the ADC side, there will be a 2.048v or 1.024v voltage reference for the analog gas sensors.
