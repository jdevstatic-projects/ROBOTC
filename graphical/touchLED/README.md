# TouchLED Sensor
These are the sample codes for `Touch LED` sensor that can be used for
several missions of your own. You must save this file as `.rbg` because
it will be read correctly by Graphical RobotC. As a raw file, it is
an XML file to be read correctly by the program, in our case,
the Graphical RobotC.

<https://raw.githubusercontent.com/xdvrx1/ROBOTC/master/graphical/touchLED/touchLED.rbg>

<https://raw.githubusercontent.com/xdvrx1/ROBOTC/master/graphical/touchLED/touchLED2.rbg>

<https://raw.githubusercontent.com/xdvrx1/ROBOTC/master/graphical/touchLED/touchLED3.rbg>

## Setup
When the physical VEX Clawbot IQ does not have all the sensors
and it is returning a port error,
you must manually remove the other sensors not present in your
Clawbot IQ in its RobotC setup.

`Motor & Sensor Setup` > `Devices`

There, you can remove the sensors by selecting `No Sensor`.

## Details
The `waitUntil` command is enough as the first line for the robot
to wait for a touch input.

`waitUntil (getTouchLEDValue(touchLED) == true);`

When there is the input, the loop will end and the program
execution will proceed to the next line. Remember, `waitUntil`
in RobotC is a loop with condition, just like `while` loop.

## Bugs
There is the possibility that the loop may not exit or
the condition might never be reached
or an `if` statement returns `false` without noticing it,
so proper algorithm should be implemented and the 
programmer must be aware of these things to avoid bugs
that can easily be prevented.

For example,

```
setTouchLEDColor(touchLED, colorGreen);
forward(1, rotations, 50);
setTouchLEDColor(touchLED, colorNone);
```

is actually correct. It seems that green is displayed
while the robot is moving forward, then will be set
to none. The `forward` command hangs the diplayed color a little
bit before being set to none. 

In case the set color command is placed
inside `if`, when testing it, before the program is run,
there must be the touch input because in less than
a second, `if` will return either `true` or `false`
based on its test and
will just skip the commands inside `if` when
the result is `false`.
