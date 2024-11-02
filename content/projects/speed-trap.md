---
title: Speed Trap

---


![](/img/projects/p2d1.png)

**Speed Trap**

The speed trap measures how fast an object is moving as it passes two sensors and display the speed on a dial-type indicator. It also relays that speed to a remote device.

The speed in cm/sec is shown on the LCD display and also on an indicator dial similar to an analog speedometer used on many cars where a pointer rotates to point to the speed. A block diagram of the speed trap is shown on the right and it has the following features:

Two LED light sources, and two phototransistors light detectors for determining the time it takes for an object to go from the first sensor to the second sensor.

An LED to indicate that a speed measurement is in progress.

An LCD display for showing the measured time to pass the sensors in msec and the speed in cm/sec. The display is also used for setting a speed threshold and displaying the speed received from the remote device.

A dial-type speedometer display for indicating the speed.

A knob for selecting a speed threshold.

A buzzer for playing an alarm tone.

A serial interface (RS-232) to another speed trap unit. When the local unit measures a speed it sends it to the remote unit. When a speed is received from the remote unit it is displayed on the LCD.

Two LEDs for comparing the speed measured on the local device with a speed received from the remote unit.

![](/img/projects/p2d2.png)

The two detectors are made from two white LEDs and two phototransistors. The LEDs and phototransistors are positioned so the light from the LED is illuminating the phototransistor unless some object blocks the path as shown below. The LEDs don't have to be controlled by the Arduino and can be wired to be on all the time. The phototransistors should each be connected to a digital input port bit and monitored using the pin change interrupts similar to how you handle the rotary encoder inputs. When the phototransistor can "see" the light from the LED the digital input will be a one. When an object blocks the light path, the input will go to a zero.
