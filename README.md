RoboFlow
============

Welcome to the repository for RoboFlow! The RoboFlow project is intended as a low-cost, open source solution to tedious, time-consuming, or previously impossible laboratory fluid handling tasks. If this sounds useful to you, read on!

A few quick facts about RoboFlow:
- Cost less than $X
- other specs
- Software, specs, etc. all freely available here.
- Build and operate yourself. There are no pre-made kits available.
- In order to build the frame, you will need to have access to a 3-D printer and laser cutter.

#General Overview
On a high level, RoboFlow physically consists of 3 stepper motors that move a nozzle around in the x-y plane, a servo that moves this nozzle in the z-direction, and a syringe pump that withdraws and dispenses fluid at the nozzle. The syringe "pump" is really just another stepper motor, connected to a lead screw that pushes/pulls on a syringe when the motor turns. The movement motors and servo are housed on a box-like frame, and the syringe pump stands outside of this area. (picture showing frame and stand)

These motors (and the servo) are all controlled by motor carrier chips, housed on either a PCB or breadboard. These motor carriers receive input from an Arduino Mega 2560. The Arduino, in turn, receives input (through its serial monitor) from a Java program running on your computer. This flow of information is shown below. (picture showing flow)

In a typical execution of RoboFlow, you simply design your experiment on the Java program, click "execute", and wait until it's done running. Under the hood, the Java and Arduino program are continuously communicating with each other (since the Arduino only knows about one small task at a time), so you should not close your Java program while the device is running.

#Getting Started
This is the main "portal" repository for RoboFlow -- the application, (etc. etc.) can be obtained by downloading this repository as a zip and unpacking it. Any questions, comments, or thoughts on the device should be directed to the [google group forums] (https://groups.google.com/forum/#!forum/roboflow).

All documentation for RoboFlow can be found in this repository's wiki pages. If you've decided you want to try RoboFlow for yourself, you should start off with the [Getting Started] (https://github.com/RoboSquirt/fluidhandler/wiki/Getting-Started) page, which contains information regarding building the device and setting up the software. From there, it is helpful to look into the [Navigating the GUI] () page.


Source Java code can be found here: https://github.com/RoboSquirt/java

Source Arduino code can be found here: https://github.com/RoboSquirt/arduino

#Remarks
Finally, a reminder. Remember that _you_ are building RoboFlow. At this point, there are no plans whatsoever in selling kits, either premade or not. Even when RoboFlow is built, it is not necessarily plug-and-play...you may need to fiddle with constants / the setup to get what is right for you and your lab. It's more than just something you make and forget -- it's a learning experience. What we hope is that you take what we have as a jump-start, share your findings with the community, and contribute in making it even better for those that make it after you. 
