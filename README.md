Modified from byrek/arduino-cj125
I moved the library files into the main dir to make it more easy to
source control and develop my project.

# Required Arduino libraries:
- SPI
- PID_v1 (arduino --install-library "PID:1.2.0")

# Example:
arduino --board arduino:avr:leonardo --verify ./arduino_cj125.ino
or
./verify

# Arduino control lines

|Arduino line|Shield|
|------------------|:--------------------------:|
|RESET|CJ125 Reset line|
|5V|5V|
|GND|GND|
|VIN|When JP1 is closed, the arduino is supplied with +/- BAT terminals|
|Analog in 0|CJ125 UA|
|Analog in 1|CJ125 UR|
|Analog in 2|Battery voltage monitoring|
|4|Analog output option (might be used to deliver O2 narrow band signal, not implemented in code)|
|5|PWM output for LSU heater|
|10|SPI CJ125 Chip select line (NSS)|
|11|SPI MOSI|
|12|SPI MISO|
|13|SPI CLK|
