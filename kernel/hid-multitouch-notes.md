# HID Multitouch Notes
Documents findings in `hid-multitouch.c` file within the Linux kernel.

## Why?
- After initially looking in `hid-input.c`, I couldn't find any mention of `BTN_STYLUS2` (the faulty button).
- I ran `git grep BARREL` and `git grep BTN_STYLUS2` within the root of the cloned Linux kernel directory.
- Those `grep` commands, returned results in several places:
  1. The `arch/microblaze/` directory which was useless to me
  2. The `drivers/hid/bpf/progs` directory, which I decided to eliminate as it was for Wacom and XP-Pen tablets, which I am not using
  3. In `drivers/hid/multitouch.c` which I decided was worth investigating.

## Findings
- Upon opening `hid-multitouch.c`, I found two places which mentioned `BARREL_SWITCH` - one for each switch.
- In both instances, the code correctly mapped the corresponding button

## Conclusion
The issue has not been as a result of a mistake within the kernel
