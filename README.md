emolab is a new control board hardware with some generic function to run and control
a model car (Carrera 1:24 style) that runs on a Carrera slotcar track.

The boards generic blocks and functionality:

- a Nordic NRF54L15 module form ezurio as core element for communication. preprogrammed with generic SW.
- an Atmega32 processor for easy maintainability by students not familiar with the zephyr system
- both processors interchange information via UART
- the board is supplied from a battery in the range of 10-20V (defined later)
- the processors each have their own LDO as power supply
- an integrated Full Bridge from Toshiba acts as motor driver for speed and direction control
- PWMs can be generated from both cores (selectable via resistor fitting)
- the board has two expansion ports to add further functionality
- the ports have all power lines and a large range of additional IO pins
- I2C and SPI are both available from both cores on the ports. The cores are selected via solder jumper
- The battery voltage can be disconnected from the driver via a PCH Mosfet
- LEDs are provided for each core and to indicate motor supply voltage is on
- The expansion port pins are such that the small standard OLED Display can be fitted directly to have a display either for ATM or from NRF
