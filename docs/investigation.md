## Initial observations

- Pen paired immediately.
- Pressure works.
- Tilt works.
- Primary barrel button works.
- Secondary barrel button activates eraser.

## Hypothesis 1

Linux incorrectly maps SecondaryBarrelSwitch.

Result: False.

hid-input.c correctly maps:

SecondaryBarrelSwitch → BTN_STYLUS2

## Hypothesis 2

The HID report contains Invert instead of SecondaryBarrelSwitch.

Result: Supported.

hid-recorder shows:

Button 1:
BarrelSwitch = 1

Button 2:
Invert = 1
SecondaryBarrelSwitch = 0
