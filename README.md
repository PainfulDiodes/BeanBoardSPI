# Hardware SPI Controller for Beanboard (Rev B)

**NOTE: this design is EXPERIMENTAL - a WORK IN PROGRESS**

Rev A was based on 74299 universal shift-register with synchronous parallel load. This was a flawed design.

In this second prototype I am returning to an earlier breadboarded design using 74165 PISO and 74164 POSI shift-registers.

I am currently testing the board and I need to review the SPI modes and which modes my devices (RA8875, W25Q) support.

---

Digital simulation files, schematics and PCB layouts for a hardware SPI controller designed to plug in to a [BeanBoard](https://github.com/PainfulDiodes/BeanBoard).

Schematic PDF: [kicad/BeanBoardSPI.pdf](kicad/BeanBoardSPI.pdf)

&nbsp;

Blog posts:

- [Breadboard SPI Controller](https://painfuldiodes.wordpress.com/2026/01/09/breadboard-spi-controller/)

- [Initial experiment writeup](https://painfuldiodes.wordpress.com/2026/01/19/hardware-spi-for-beanboard/)

- [PCB Build and a Timing Puzzle](https://painfuldiodes.wordpress.com/2026/02/27/beanboard-spi-pcb-build-and-a-timing-puzzle/)

&nbsp;

Thank you to those helpful folks at [PCBWay](https://pcbway.com) who sponsored this build and provided the PCBs!

&nbsp;

![beanboardspi-revb-populated](images/beanboardspi-revb-populated.jpg)
Rev B - BeanBoardSPI populated with Adafruit SPI modules

![beanboardspi_populated](images/beanboardspi_populated.jpg)
Rev A - BeanBoardSPI populated with Adafruit SPI modules

![beanboard-spi-pcb-assembled](images/beanboardspi-pcb-assembled.jpg)
Rev A - Plugged into BeanBoard with BeanZee, and a TFT panel

![beanboard-spi-breadboard](images/beanboardspi-breadboard.jpg)
Breadboarding
