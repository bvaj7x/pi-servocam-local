# Hardware Plan

This document captures the current hardware state and the planned
hardware direction for `pi-servocam-local`. It is intentionally
conservative until parts, wiring, and power behavior are confirmed.

## Current Hardware

- Raspberry Pi 5
- Raspberry Pi Camera Module 3

## Already Selected

- Main computer: Raspberry Pi 5
- Current camera target: Raspberry Pi Camera Module 3
- Current implementation target: Camera Module 3 bring-up
- Network model: local LAN only, once the camera view exists
- First-stage power model: wall power, no battery

## Still To Choose

- Exact servo models
- Servo power supply rating
- Pan/tilt bracket or mount
- Camera cable length and routing
- Case or enclosure, if needed
- Optional battery or power pack for a later stage

## Planned Later

- Two servos for pan/tilt movement
- Pan/tilt mount
- Separate servo power supply if needed
- Optional battery or power pack

## Power Notes

There are no servos in the current hardware set.

When servos are added later, do not power powerful servos directly from
the Raspberry Pi 5V pin as a default design.

Servos can draw high current during startup, movement, or stall
conditions. For anything beyond very small test servos, a separate servo
power supply is usually the safer path. The Raspberry Pi and servo supply
should share a common ground so control signals have the same reference.

The final power plan should be documented before the wiring guide is
treated as build-ready.

## Wiring Status

No confirmed pinout is documented yet.

That is deliberate: exact GPIO pins, servo power wiring, and camera cable
routing should be written down after the selected servos, controller
approach, and mechanical layout are known.

Camera Module 3 bring-up should be documented first, after it is tested
on the Raspberry Pi 5.

## Mechanical Notes

The first version does not need a pan/tilt bracket or polished enclosure.

When pan/tilt hardware is added later, the project should leave space for:

- Servo travel limits
- Camera cable strain relief
- Heat and airflow around the Raspberry Pi
- Stable mounting on a desk, shelf, tripod, or wall bracket
