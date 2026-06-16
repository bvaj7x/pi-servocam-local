# Roadmap

`pi-servocam-local` is planned in small phases so the project stays understandable while hardware and software are brought up.

## P0 - Documentation

Goal: make the project legible before implementation.

- [x] repo documentation
- [ ] hardware wiring plan
- [ ] confirm initial hardware choices
- [ ] document local-only network assumptions

## P1 - Camera Stream

Goal: bring up the camera path on Raspberry Pi 5.

- [ ] camera bring-up
- [ ] confirm Raspberry Pi Camera Module 2 or 3 setup
- [ ] choose the first streaming approach
- [ ] document tested camera commands after they exist
- [ ] expose a basic local view when implementation starts

## P2 - Servo Pan/Tilt

Goal: add controlled two-axis movement safely.

- [ ] pan/tilt servo control
- [ ] choose servo models and power supply
- [ ] document confirmed wiring
- [ ] add movement limits
- [ ] add calibration
- [ ] verify mechanical range before polish

## P3 - Polished Local Device

Goal: turn the prototype into a pleasant local LAN device.

- [ ] local web UI
- [ ] systemd service
- [ ] simple device setup notes
- [ ] optional enclosure
- [ ] optional battery/power pack
- [ ] final safety and maintenance notes

## Guiding Rule

Do not pretend a feature exists before it has been tested. Documentation should say what is planned, what is known, and what still needs proof.
