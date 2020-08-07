# Line Tracking

## Code
```
task main()
{
	// For the case of `Try It: Line Tracking`,
	// we must use lineTrackRight.
	//// Why?
	// Remember, the `High Speed` will be applied to the right motor
	// when the Color sensor sees light shade,
	// hence it will turn right when secondary speed is 0.
	repeat (forever) {
		lineTrackRight(colorDetector, 50, 50, 0);
	}
}
```

## Setup
In Robot Virtual World, this corresponds to `Try It: Line Tracking`.
This can be manually setup for the physical field.

## Details
Depending on the setup, either you will be tracking right or left.
Take note of the High Speed, it is the driving force whether it will
go left or right.
