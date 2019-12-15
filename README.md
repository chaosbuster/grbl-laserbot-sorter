# grbl-makeblock-sorter
fork of grbl-laserbot. Customizations of a Makeblock Laserbot with Mega Pi board to sort items


# Installation

Connect the Mega Pi
Start your Arduino IDE and open the Arduino.ino file in the /Arduino subdirectory of this repostiory.

Make sure that you selected the board "Arduno/Genuino Mega or Mega 2560" in your Arduino IDE and select the serial port that connects to your Mega Pi.

Upload the sketch.

# Configuration


The axis that carries the pick-n-sorter is the y-axis. The other axis is the x-axis. Make sure, that the endstop, that the x-axis runs into is connected to the first "servo port" and the endstop for the y-axis is connected to the second "servo port".  The Z-axis is the pick-n-sorter which should be connected to the third "servo port".

Limit switches for all axis are being used.

The following configuration is used and you can find it in the file laserbot.nc in this repository:
```
$0=10 (Step pulse time)
$1=255 (Step idle delay)
$2=0 (Step pulse invert)
$3=2 (Step direction invert)
$4=0 (Invert step enable pin)
$5=0 (Invert limit pins)
$6=0 (Invert probe pin)
$10=1 (Status report options)
$11=0.020 (Junction deviation)
$12=0.002 (Arc tolerance)
$13=0 (Report in inches)
$20=0 (Soft limits enable)
$21=0 (Hard limits enable)
$22=1 (Homing cycle enable)
$23=11 (Homing direction invert)
$24=500.000 (Homing locate feed rate)
$25=2000.000 (Homing search seek rate)
$26=250 (Homing switch debounce delay)
$27=5.000 (Homing switch pull-off distance)
$30=0 (Maximum spindle speed)
$31=0 (Minimum spindle speed)
$32=0 (Was Laser-mode enable)
$100=25.750 (X-axis travel resolution)
$101=25.750 (Y-axis travel resolution)
$102=25.750 (Z-axis travel resolution)
$110=18000.000 (X-axis maximum rate)
$111=20000.000 (Y-axis maximum rate)
$112=300.000 (Z-axis maximum rate)
$120=400.000 (X-axis acceleration)
$121=1000.000 (Y-axis acceleration)
$122=100.000 (Z-axis acceleration)
$130=360.000 (X-axis maximum travel)
$131=350.000 (Y-axis maximum travel)
$132=50.000 (Z-axis maximum travel)
```


# General notes

Pick-n-sorter uses LEGO worm gears and a 3D Printed mount where the laser was connected

Sorting area: Up to 383mm×367mm

MegaPi uses	DRV8825		


# Usage with OpenPnP

Install from http://openpnp.org

Select the right serial port and upload the settings from laserbot.nc from this repository.

You can now send your gcode to your pick-n-sorter. You can check by turning on the machine in OpenPnp then click the Homing button to see if it will run and find the homing positions for all 3 axis.


# MegaPi Pin mapping

```									
							
```
