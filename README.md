# Land_Meter_C
Land Meter Embedded Program in C
Book:
http://exploringbeaglebone.com/
http://exploringbeaglebone.com/API/ExploringBeagleBoneAPI.pdf



C Libraries
http://blacklib.yigityuce.com/downloads.html


http://beagleboard.org/project/BBB/


PWM:
https://groups.google.com/forum/#!topic/beagleboard/dkS51WbicTo


PID:

https://github.com/gregorygusberti/PID
https://github.com/nicholastmosher/PID
https://github.com/tekdemo/MiniPID


PRU:
http://exploringbeaglebone.com/chapter13/
https://github.com/Greg-R/pru-pid-motor

http://processors.wiki.ti.com/index.php/PRU_Training:_Hands-on_Labs
http://beagleboard.org/pru
https://www.element14.com/community/community/designcenter/single-board-computers/next-gen_beaglebone/blog/2013/05/22/bbb--working-with-the-pru-icssprussv2
https://beagleboardfoundation.wordpress.com/2016/12/31/motor-speed-control-using-beaglebone-pru/

Other:

http://derekmolloy.ie/tag/beaglebone-black/

https://press3.mcs.anl.gov/forest/hardware/beaglebone-black-software/examples-and-tutorials/


SPI:
https://www.linux.com/learn/how-access-chips-over-spi-beaglebone-black
http://www.ofitselfso.com/BBBCSIO/Help/BBBCSIOHelp_SPIPortExample.html


I2C:
http://beagleboard.org/project/bbb_i2c/


UART:


Interrupts:


SSD1306:

https://github.com/jeromelebel/BeagleBone-SSD1306
http://guy.carpenter.id.au/gaugette/2014/01/28/controlling-an-adafruit-spi-oled-with-a-beaglebone-black/
https://sourceforge.net/p/bonelib/wiki/SSD1306.hpp/



Should we store cal, offsets, etc. on Android or BBB?

Flow:
1)  Configure pins
2)  Load setup info from file, setup GPIO
3)  Power up system + settling time
4)  System voltage check, setup UART, SPI, PWM etc
5)  Log issues, set sys not ready flag, heater
6)  Begin main{}
7)  Heaters, update heater ready flag
8)  Levels, update levels ready flag.  Update every 0.1 sec.
9)  Check for comm
10) Shaft positioning, encoder, arrestment motor, update status and position when complete
11) Set PWM
12) Check beam position









