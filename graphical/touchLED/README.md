# Mission
These are sample codes for `Touch LED` sensor. This can be used for
several missions of your own.

## Setup
When the VEX Clawbot IQ does not contain all the sensors,
you must manually remove the other sensors not present in your
Clawbot IQ.

`Motor & Sensor Setup` > `Devices`

There, you can remove the sensors by selecting `No Sensor`.

## Details
The `waitUntil` command is enough as the first line for the robot
to wait for a touch input.

`waitUntil (getTouchLEDValue(touchLED) == true);`

When there is already the input, the loop will end and the program
execution will proceed to the next line.

## Bugs
There is the possibility that the loop may not exit or
the condition might never be reached, so proper algorithm
should be implemented.

For example,

```
setTouchLEDColor(touchLED, colorGreen);
forward(1, rotations, 50);
setTouchLEDColor(touchLED, colorNone);
```

is actually correct. It seems that green is there
while the robot is moving forward, then will be set
to none. When this command 

`setTouchLEDColor(touchLED, colorNone);`

is placed as the first line inside `Repeat Forever`,
then the green light will not be displayed while the robot
is moving forward.
