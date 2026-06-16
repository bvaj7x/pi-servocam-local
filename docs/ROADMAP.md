# Roadmap

`pi-servocam-local` is planned in small phases so the project stays
understandable while hardware and software are brought up.

## P0 - Documentation

Goal: make the project legible before implementation.

- [x] repo documentation
- [ ] hardware wiring plan
- [ ] confirm initial hardware choices
- [ ] document local-only network assumptions

## P1 - Camera Module 3 Bring-Up

Goal: prove the current camera hardware on Raspberry Pi 5.

- [ ] connect Raspberry Pi Camera Module 3
- [ ] confirm Camera Module 3 detection on Raspberry Pi 5
- [ ] document tested camera setup steps after they exist
- [ ] keep untested commands out of the documentation

## P2 - Local LAN Camera View

Goal: expose the camera locally after bring-up is confirmed.

- [ ] choose the first local camera view approach
- [ ] expose a basic camera view on the local network
- [ ] document tested local access steps after they exist
- [ ] keep the prototype local-only by default

## P3 - Pan/Tilt Hardware Selection

Goal: choose the movement hardware after the camera path is understood.

- [ ] choose servo models
- [ ] choose a pan/tilt mount
- [ ] decide whether separate servo power is needed
- [ ] document confirmed wiring only after hardware is selected

## P4 - Servo Control And Calibration

Goal: add controlled two-axis movement safely.

- [ ] pan/tilt servo control
- [ ] document confirmed wiring
- [ ] add movement limits
- [ ] add calibration
- [ ] verify mechanical range before polish

## P5 - Optional Enclosure/Battery

Goal: make the device more self-contained after the core prototype works.

- [ ] optional enclosure
- [ ] optional battery/power pack
- [ ] simple device setup notes
- [ ] final safety and maintenance notes

## Guiding Rule

Do not pretend a feature exists before it has been tested. Documentation
should say what is planned, what is known, and what still needs proof.
