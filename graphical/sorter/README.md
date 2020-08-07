# Sorter Challenge

## Code

```
task main()
{
	repeat (4) {
		moveMotor(clawMotor, 1, seconds, -100);
		wait(2, seconds);
		setMultipleMotors(50, leftMotor, rightMotor, noMotor, noMotor);
		waitUntil (getDistanceValue(distanceMM) &lt;= 70);
		stopAllMotors();
		moveMotor(clawMotor, 1, seconds, 100);
		wait(2, seconds);
		if (getColorName(colorDetector) == colorGreen) {
			turnRight(250, degrees, 50);
			moveMotor(clawMotor, 1, seconds, -100);
			turnLeft(250, degrees, 50);
		} else {
			turnLeft(250, degrees, 50);
			moveMotor(clawMotor, 1, seconds, -100);
			turnRight(250, degrees, 50);
		}
		stopAllMotors();
		moveMotor(clawMotor, 1, seconds, 100);
	}
}
```

## Setup
This corresponds to the Strawberry Sorter Challenge in the RVW.
Color is best performed, particularly when dealing with color hue
and color name, in the virtual world.

## Details
The task of the robot is to sort the plants according to its mark.
Either it will be placed on the left or the right side. For every set,
the marks are given without any pattern.
