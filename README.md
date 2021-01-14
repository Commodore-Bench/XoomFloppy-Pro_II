# XoomFloppy Pro II



![](https://github.com/DL2DW/XoomFloppy-Pro_II/blob/main/Images/XoomFloppy_Pro_II.jpg)



In 2018, I had developed the first [XoomFloppy Pro](https://github.com/DL2DW/XoomFloppy_Pro_2018). A XUM1541, but which is 100% compatible with the [ZoomFloppy](http://store.go4retro.com/zoomfloppy/) and also requires the same firmware.

Over time, I had then made some improvements. So I have now attached all components on the upper side. Then I added a Centronics connector for the IEEE-488 interface, so that the usual standard GPIB cables can be used. 

This made the XoomFloppy Pro II a little bit wider, and it is now 99,6 x 50,3mm (ZoomFloppy = 118,3x77,5mm). This is still within the size that is fairly inexpensive from the board manufacturers.



## Interfaces

On the one hand there is the CBM bus known from the VIC20, C64 and C128 in form of the 6pin DIN socket. In addition, the connection for a floppy speeder with parallel cable is available as a PCB connector (analog to the user port of the C64/C128), as well as a DSUB25 connector.

Furthermore, an IEEE-488 (GPIB) interface is on board, which is also available as a platinum connector (like on the PET and CBM devices), Centronics socket and pin header (IDC connector).

Of course, only one of the two interfaces can be used at a time. So either CBM bus with additional parallel cable OR IEEE-488.




## Assembly

![](https://github.com/DL2DW/XoomFloppy-Pro_II/blob/main/Images/XoomFloppy_Pro_II_PCB_top.jpg)



First of all, the SMD parts should be assembled in descending order of size. So first the ATMega, then the 75LS06, etc. 

And only then the sockets and connectors. I have left as much space as possible between the individual components, so that even less experienced should be able to assemble this board without problems.

For overview a 3D picture of the assembled board:

![](https://github.com/DL2DW/XoomFloppy-Pro_II/blob/main/Images/XoomFloppy_Pro_II_PCB_3D.jpg)



The completely assembled board looks like this:

![](https://github.com/DL2DW/XoomFloppy-Pro_II/blob/main/Images/XoomFloppy_Pro_II_PCB_assembled_top.jpg)



## Firmware

The [firmware](https://github.com/OpenCBM/OpenCBM) is flashed via USB analog to the ZoomFloppy. The [openCBM](https://spiro.trikaliotis.net/Download/opencbm-0.4.99.103/opencbm-0.4.99.103.zip) package is required for operation. The instructions for openCBM can be found at https://opencbm.trikaliotis.net/



## BOM

Here is the list of components needed. I have chosen the manufacturers as examples. Of course, compatible components from other manufacturers can also be selected.

| Quantity | Designator          | Manufacturer         | Manufacturer  Part Number  | Description                                                  |
| -------- | ------------------- | -------------------- | -------------------------- | ------------------------------------------------------------ |
| 1        | C5                  | KEMET                | C0603C105K3RACTU           | KEMET  1F Multilayer Ceramic Capacitor (MLCC) 25 V 10% X7R dielectric C SMD max op.  temp. +125C |
| 1        | CN1                 | HARTING  Technology  | 09642237802                | HARTING     09 64 223 7802       Filtered D Sub Connector,  Ferrite, DA, Plug, 15 Contacts, 0 F, Steel Body |
| 1        | CN2                 | Wurth  Electronics   | 629105150521               | Socket  micro-USB B 5P, 629105150521, Würth Elektronik       |
| 1        | CN3                 | Lumberg              | 010599  06                 | DIN  chassis socket, right angle version, with ground contact, suitable for  locking, for printed circuit boards |
| 1        | CN6                 | L-Com                | CIB24SRA                   | L-COM  - CIB24SRA - CONNECTOR GPIB R/A FEMALE                |
| 1        | CN7                 | Samtech  Inc.        | TST-112-01-G-D             | IEEE-488 IDC  Connector Right Angle or Straight              |
| 1        | D1                  | Wurth  Electronics   | 150060BS55040              | LED  BLUE DIFFUSED 0603 SMD                                  |
| 1        | D2                  | Wurth  Electronics   | 151033BS03000              | WURTH  ELEKTRONIK  151033BS03000  LED, 3MM, BLUE, 3800MCD, 470NM |
| 1        | DZ1                 | STMicroelectronics   | USBLC6-2SC6                | TVS  DIODE 5.25V 17V SOT23-6                                 |
| 1        | F1                  | Littelfuse           | 1206L150THWR               | PTC  RESET FUSE 8V 1.5A 1206                                 |
| 1        | R1                  | Yageo                | RC0603FR-0710KL            | RES  SMD 10K OHM 1% 1/10W 0603                               |
| 1        | R8                  | Yageo                | RC0603FR-07220RL           | RES  SMD 220 OHM 1% 1/10W 0603                               |
| 1        | U1                  | Texas  Instruments   | SN74LS06DR                 | IC  INVERTER OPEN COL 6CH 14SOIC                             |
| 1        | U2                  | Microchip  / Atmel   | ATMEGA32U2-AU              | ATMEL     ATMEGA32U2-AU      MCU, 8BIT, MEGAAVR, 16MHZ,  TQFP-32 |
| 1        | Y1                  | Raltron  Electronics | R2016-16.000-9-1010-TR-NS1 | 16MHz  ±10ppm 9pF 200Ω SMD,2.0x1.6mm SMD Crystal Resonators RoHS |
| 2        | C3,  C4             | KEMET                | C0603C220J5RACTU           | 22.0PF  50.0V                                                |
| 2        | R3,  R4             | Yageo                | RC0603FR-0722RL            | RES  SMD 22 OHM 1% 1/10W 0603                                |
| 2        | RN1,  RN2           | Yageo                | TC124-FR-07100KL           | RES  ARRAY 4 RES 100K OHM 0804                               |
| 3        | C1,  C2, C6         | KEMET                | C0603C104J3RACTU           | KEMET     C0603C104J3RACTU       SMD Multilayer Ceramic  Capacitor, 0603 [1608 Metric], 0.1 F, 25 V,   5%, X7R, C Series |
| 5        | R2,  R5, R6, R7, R9 | Yageo                | RC0603FR-074K7L            | RES  SMD 4.7K OHM 1% 1/10W 0603                              |



## PCB

The PCB can either be ordered directly from [PCBWay](https://www.pcbway.com/project/shareproject/XoomFloppy_Pro_II.html), or you can create it yourself from the Gerber files available here.

[![PCBWay](https://www.pcbway.com/project/img/images/frompcbway.png)](https://www.pcbway.com/project/shareproject/XoomFloppy_Pro_II.html)



If you liked my project, I would be very happy about a small coffee donation.

[![ko-fi](https://www.ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/R6R62T6RN)



# License

The contents of this repository, with the exception of the Docs and Software directories, are released under the following license:

- the "Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License" (CC BY-NC-SA 4.0) full text of this license is included in the [LICENSE.CC-NC-BY-SA-4.0](https://github.com/DL2DW/XoomFloppy-Pro_II/blob/main/LICENSE.CC-NC-BY-SA) file and a copy can also be found at https://creativecommons.org/licenses/by-nc-sa/4.0/
