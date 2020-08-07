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

## Details
