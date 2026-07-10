# Hardware SPI Controller for Beanboard (Rev A)

**NOTE: this revision is flawed, but is retained for reference**

There is a problem with the SPI clock. There are jumpers to allow selection of division of the CPU clock (10MHz): /1 /2 /4. I expected to use CLK/4 (2.5 MHz), but this exposed a defect in the design.

At CLK/4 (2.5 MHz) the WR pulse ends before the required rising SCLK edge. This is a problem with using a synchronous load on the shift register.

The board does appear to function correctly at CLK/2, but it is technically out of range for the RA8875 controller.

In addition, implicit in the design is that the shif-register clocks (in and out) are tied together. For SPI we need to sample the input out of phase to the SPI clock, which allows the input to stabilize before sampling - which is not possible in this design. 

---

Digital simulation files, schematics and PCB layouts for a hardware SPI controller designed to plug in to a [BeanBoard](https://github.com/PainfulDiodes/BeanBoard).

Blog posts:

- [Initial experiment writeup](https://painfuldiodes.wordpress.com/2026/01/19/hardware-spi-for-beanboard/)

- [PCB Build and a Timing Puzzle](https://painfuldiodes.wordpress.com/2026/02/27/beanboard-spi-pcb-build-and-a-timing-puzzle/)

&nbsp;

Thank you to those helpful folks at [PCBWay](https://pcbway.com) who sponsored this build and provided the PCBs!

&nbsp;

![beanboardspi_populated](images/beanboardspi_populated.jpg)
BeanBoardSPI populated with Adafruit SPI modules

![beanboard-spi-pcb-assembled](images/beanboardspi-pcb-assembled.jpg)
Plugged into BeanBoard with BeanZee, and a TFT panel

![beanboard-spi-breadboard](images/beanboardspi-breadboard.jpg)
Breadboarding

![beanboard-spi-interface](kicad/BeanBoardSPI.png)
