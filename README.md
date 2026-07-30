# ASUS ROG Flow Z13 Linux Pen Investigation

An investigation into a compatibility issue between the ASUS ROG Flow Z13 (ELAN9008:00 / 04F3:41EB) digitiser and the Renaisser Raphael 520C MPP pen under Linux.

## Summary

Pressing the second side button causes Linux to activate the eraser tool instead of reporting a secondary stylus button.

This repository documents the investigation into the issue, including:

- HID descriptor analysis
- Runtime HID captures
- Linux kernel source analysis
- Experimental results
- Potential root causes

No conclusions should be considered final until confirmed upstream.
