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
