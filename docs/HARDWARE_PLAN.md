# Hardware Plan

This document captures the initial hardware direction for `pi-servocam-local`. It is intentionally conservative until parts, wiring, and power behavior are confirmed.

## Initial Hardware List

- Raspberry Pi 5
- Raspberry Pi Camera Module 2 or Raspberry Pi Camera Module 3
- Two servos for pan/tilt movement
- Standard wall power supply for the Raspberry Pi
- Local network connection through Ethernet or Wi-Fi

## Already Selected

- Main computer: Raspberry Pi 5
- Camera family: Raspberry Pi Camera Module 2 or 3
- Movement concept: two-axis pan/tilt using two servos
- Network model: local LAN only
- First-stage power model: wall power, no battery

## Still To Choose

- Exact camera module version
- Exact servo models
- Servo power supply rating
- Pan/tilt bracket or mount
- Camera cable length and routing
- Case or enclosure, if needed
- Optional battery or power pack for a later stage

## Power Notes

Do not power powerful servos directly from the Raspberry Pi 5V pin as a default design.

Servos can draw high current during startup, movement, or stall conditions. For anything beyond very small test servos, a separate servo power supply is usually the safer path. The Raspberry Pi and servo supply should share a common ground so control signals have the same reference.

The final power plan should be documented before the wiring guide is treated as build-ready.

## Wiring Status

No confirmed pinout is documented yet.

That is deliberate: exact GPIO pins, power wiring, and camera cable routing should be written down after the selected servos, controller approach, and mechanical layout are known.

## Mechanical Notes

The first version can use a simple pan/tilt bracket or prototype mount. A polished enclosure is not required for early bring-up, but the project should leave space for:

- Servo travel limits
- Camera cable strain relief
- Heat and airflow around the Raspberry Pi
- Stable mounting on a desk, shelf, tripod, or wall bracket
