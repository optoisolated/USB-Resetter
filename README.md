# USB Resetter

The USB Resetter allows for using a 5V power source such as a GPIO Pin on a Raspberry Pi or Arduino to enable/disable a USB A connection. This was designed to facilitate allowing my Raspberry Pi to Reset my Fine Offset Weather Station which suffers from USB Lockup, and the only recourse is to forcibly power-cycle the device. 

This device uses a Male and Female USB-A connection to allow for simple installation, and then a 2 PIN GPIO-Compatible input for the reset. The circuit is normally open, so requires power to enable the USB. The device only switches the VBUS Pin on the USB device, so the data pins are not hindered in any way by active circuitry; which may reduce throughput.
