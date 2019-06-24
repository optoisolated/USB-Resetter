# USB Resetter

The USB Resetter allows for using a 5V power source such as a GPIO Pin on a Raspberry Pi or Arduino to enable/disable a USB A connection. This was designed to facilitate allowing my Raspberry Pi to Reset my Fine Offset Weather Station which suffers from USB Lockup, and the only recourse is to forcibly power-cycle the device. 

This device uses a Male and Female USB-A connection to allow for simple installation, and then a 2 PIN GPIO-Compatible input for the reset. The circuit is normally open, so requires power to enable the USB. The device only switches the VBUS Pin on the USB device, so the data pins are not hindered in any way by active circuitry; which may reduce throughput.

The Power Switching circuit uses an optically isolated Solid State Relay to minimise power loss and ensure a clean power transition. The on/off pins directly connect to the LED side of the Optocoupler and are not driven in any way by the USB power line. This ensures no power loss due to the optoisolator LED and also ensures no shared ground between the the USB line and the device performing the switching. 

The ASSR-1218 SSR has been assumed to be run between 3.3v and 5v and has as an in-series resistor to accomodate that. The line can be driven with a higher voltage but will need an appropriate voltage divider and circuit protection. The SSR will draw between 2mA and 20mA in normal operation. The on/off pins are not latched, so need to driven to remain on.

The Bypass switch is driven by the VBUS line and does not need any external power connected in order to work. 

Note that with the Bypass switch in the on position, the On/Off pins will have no effect.
