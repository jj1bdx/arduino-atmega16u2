# Arduino 16u2 USB chip firmware

## Sources

* `hardware/arduino/avr/firmwares/atmegaxxu2` at <https://github.com/arduino/Arduino>
* `firmware/atmega16u2` at <https://github.com/Pinoccio/hardware-pinoccio>

## How to build

    # DFU bootloader
    (cd Bootloaders/arduino-usbdfu && make clean && make)
    # USB serial firmware
    (cd Projects/arduino-usbserial && make clean && make)

## Note very well

* The LUFA version is 100807, as in the hardware-pinoccio repository. This version is required for both DFU and USB serial firmware.

## References

* LUFA source: https://github.com/abcminiuser/lufa
