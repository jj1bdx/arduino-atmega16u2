# Arduino usbserial application firmware

To setup the project and upload the Arduino usbserial application firmware to an ATmega16U2 using the Arduino USB DFU bootloader:

1. unpack the source into LUFA's Projects directory
2. set `ARDUINO_MODEL_PID` in the makefile as appropriate
3. do `make clean; make`
4. put the 16U2 into USB DFU mode (shown in a later section)
5. confirm that the board enumerates as either "Arduino Uno DFU" or "Arduino Mega 2560 DFU"
6. do `make dfu` (OS X or Linux - dfu-programmer must be installed first) or `make flip` (Windows - Flip must be installed first)

Check that the board enumerates as either "Arduino Uno" or "Arduino Mega 2560".  Test by uploading a new Arduino sketch from the Arduino IDE.

## How to put ATmega8u2/16u2 into USB DFU mode

1. assert and hold the 16U2's RESET line
2. assert and hold the 16U2's HWB line
3. release the 16U2's RESET line
4. release the 16U2's HWB line

