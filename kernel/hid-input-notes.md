# HID Input Notes
Documents findings in `hid-input.c` file within the Linux kernel

## Inspecting the code
Search for mentions of `HID_DG_BARRELSWITCH`, `HID_DG_SECONDARYBARRELSWITCH`, `HID_DG_INVERT` and `HID_DG_ERASER` in `hid-input.c`

- Found no mentions of `HID_DG_BARRELSWITCH` or `HID_DG_SECONDARYBARRELSWITCH` -> must be controlled by another `.c` file
- `HID_DG_INVERT` and `HID_DG_ERASER` both present. When code detects `invert` (i.e. the stylus being flipped around), the eraser tool is activated.
