# Morserino-32 with Load Sensor Paddles

This is a **fork** of Morserino-32 multi-functional Morse code machine, based on ESP32.

### Built-in capacitive touch sensors are replaced with load sensor (weight sensor) using CS1237 ADC. ###
Load Sensor paddles have better reliability compared to capacitive touch paddle, they behave like noiseless mechanical paddle, no need to always touch a particular spot on the sensor. Finger does not need to be removed, it is sufficient to decrease pressure as load sensor has inherent spring action.
**For more details see https://blog.hb9txb.ch**

**Hardware additions**:
- ESP32 free pin 13 configured as CLK for ADC sensors, one wire soldered
- Pins 2 and 12 formerly used for capacitive touch paddle configured as DATA for two ADC 
- GND and 3.3VEXT taken from JMP1 free holes.
- Breadboard with 2 x CS1237 ADC plus two load sensors

As there were no free pins on ESP32,  load sensor had to be enabled at compilation using preprocessor directive `#define FEATURE_PRESSURE_PADDLES` in `morsedefs.h` replacing original capacitive touch functionality.

![Morserino Image](https://raw.githubusercontent.com/djbr1/Morserino-32/master//Documentation/Hardware/IMG_1763.JPG?raw=true)

Load sensor paddles sensitivity can be changed using `m32command` syntax through web serial. It works through serial console (eg picocom, minicom, putty) or using browser (Chrome,Opera or Edge).
Controls for sensitivity are supported in Morserino code and in HTML pages<br>
`GET control/pressure_threshold_dot`<br>
`GET control/pressure_threshold_dash`<br>
`PUT control/pressure_threshold_dot`<br>
`PUT control/pressure_threshold_dash`<br>

[My fork of Christof Dallermassl OE6CHD Morserino CW trainer](https://github.com/djbr1/morserino32-trainer) provides [HTML](https://github.com/djbr1/morserino32-trainer/blob/main/sensor.html) for this purpose

![web serial console screenshot](https://github.com/djbr1/Morserino-32/blob/master/Documentation/Hardware/sensor.html.jpg?raw=true)

<br>
<!--TODO: 
- single lever functionality ie using just one load sensor - preferred by HST competitors.  -->

[![morserino32 shorts youtube](https://img.youtube.com/vi/P5Paj6hcao0/0.jpg)](https://www.youtube.com/watch?v=P5Paj6hcao0)




------------------------------------------
<br><br><br>

# Morserino-32
Morserino-32 multi-functional Morse code machine, based on ESP32

Here on GitHub you will find both software and documentation of both hardware and software.

For more information about original Morserino-32, and for buying a kit, go to http://bit.ly/morserino-32

For general information and FAQ go to http://morserino.info

Announcements via Email (through Mailchimp): http://eepurl.com/dwEVkz

User Group (Email, through groups.io): https://groups.io/g/morserino

![Morserino Image](https://raw.githubusercontent.com/oe1wkl/Morserino-32/master/Documentation/User%20Manual/Version%204.x/Morserino.jpg)

![DXZone logo](https://raw.githubusercontent.com/oe1wkl/Morserino-32/master/dxzone_180x85_rounded.gif)

<a href="https://www.dxzone.com/cgi-bin/dir/rate.cgi?ID=33277">Rate this site @ dxzone.com</a>
