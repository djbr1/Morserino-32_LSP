# Morserino-32 with Load Sensor Paddles

This is a **fork** of Morserino-32 multi-functional Morse code machine, based on ESP32.

### Built-in capacitive touch sensors are replaced with load sensor (weight sensor) using CS1237 ADC. ###
Load Sensor paddles have better reliability compared to capacitive touch paddle, they behave like noiseless mechanical paddle, mot requiring touching of particular spot. 
Finger does not need to be removed, it is sufficient to decrease pressure as load sensor has inherent spring action.

Hardware:
- ESP32 free pin 13 configured as CLK for ADC sensors, one wire soldered
- Pins 2 and 12 formerly used for capacitive touch paddle configured as DATA for two ADC 
- GND and 3.3VEXT taken from JMP1 free holes.
- 2 x CS1237 ADC on breadboard plus two load sensors

As there were no free pins on ESP32,  load sensor had to be enabled at compilation using preprocessor directive `#define FEATURE_PRESSURE_PADDLES` in `morsedefs.h` replacing original capacitive touch functionality.

TODO: 
load sensor configurations: (preferably through webserial https://tegmento.org/#m32-config-device )
- load sensor paddles sensitivity 
- single lever option:  load sensor provides "negative" weight if pressure applied in counter direction thus allowing single ADC and single load sensor configuration for those who prefer non-iambic.


![Morserino Image](https://raw.githubusercontent.com/djbr1/Morserino-32/master//Documentation/Hardware/IMG_1763.JPG?raw=true)


------------------------------------------
<br><br><br>


Here on GitHub you will find both software and documentation of both hardware and software.

For more information about original Morserino-32, and for buying a kit, go to http://bit.ly/morserino-32

For general information and FAQ go to http://morserino.info

Announcements via Email (through Mailchimp): http://eepurl.com/dwEVkz

User Group (Email, through groups.io): https://groups.io/g/morserino

![Morserino Image](https://raw.githubusercontent.com/oe1wkl/Morserino-32/master/Documentation/User%20Manual/Version%204.x/Morserino.jpg)

![DXZone logo](https://raw.githubusercontent.com/oe1wkl/Morserino-32/master/dxzone_180x85_rounded.gif)

<a href="https://www.dxzone.com/cgi-bin/dir/rate.cgi?ID=33277">Rate this site @ dxzone.com</a>
