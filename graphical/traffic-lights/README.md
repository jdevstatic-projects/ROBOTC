# Traffic Lights
## Code

```
task main()
{
	repeat (forever) {
		if (getColorName(colorDetector) == colorRed) {
			stopAllMotors();
		} else {
			setMultipleMotors(20, leftMotor, rightMotor, noMotor, noMotor);
		}
	}
}
```

## Setup
This corresponds to the traffic lights in the virtual world. This uses
the color sensor of the robot, either color hue or color name.

## Details
We used `repeat(forever)` as the main loop. Inside that is the `if-else`
conditional statement to decide whether the input is either red or not red.
Depending on the color, it will either move forward or stop.
